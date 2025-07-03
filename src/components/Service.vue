<script setup lang="ts">
const services = ref([
    {
        icon: 'fa-solid:clinic-medical',
        title: 'Facelift Procedure',
        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum harum placeat commodi aliquam',
        link: 'facelift'
    },
    {
        icon: 'fa-solid:clinic-medical',
        title: 'Facelift Procedure',
        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum harum placeat commodi aliquam',
        link: 'facelift'
    },
    {
        icon: 'fa-solid:clinic-medical',
        title: 'Facelift Procedure',
        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum harum placeat commodi aliquam',
        link: 'facelift'
    },
    {
        icon: 'fa-solid:clinic-medical',
        title: 'Facelift Procedure',
        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum harum placeat commodi aliquam',
        link: 'facelift'
    },
    {
        icon: 'fa-solid:clinic-medical',
        title: 'Facelift Procedure',
        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rerum harum placeat commodi aliquam',
        link: 'facelift'
    }
])
</script>

<template>
    <section id="service" class="py-20 overflow-hidden bg-gradient-to-r from-pink-100 to-purple-100">
     <div class="container mx-auto px-4">
      <header data-aos="fade-up" data-aos-dalay="500" class="text-center mb-16">
        <h2 id="service-heading" class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
            Our <span class="text-pink-600">Premium Service</span>
        </h2>
        <p class="text-lg text-gray-600 max-w-2xl mx-auto">
            Discover our rang of specialized cosmetic treatments design to enhanch your natural beauty
        </p>
      </header>

      <ul data-aos="fade-up" data-aos-dalay="500" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <li v-for="(service, index) in services" :key="index">
            <article class="bg-white rounded-xl p-8 hover:shadow-lg transition:all duration-300
            hover:translate-y-[-5px] h-full flex flex-col">
                <figure class="mb-6">
                    <Icon :icon="service.icon" class="text-4xl text-pink-600" aria-hidden="true"></Icon>
                </figure>
                <h3 class="text-xl font-bold text-gray-800 mb-3">
                    {{ service.title }}
                </h3>
                <p class="text-gray-600 mb-6 flex-grow">
                    {{ service.description }}
                </p>
                <a :href="service.link"
                class="group inline-flex items-center gap-2 text-pink-600 font-semibold"
                >
                 <span class="relative">
                    Learn more
                    <span class="absolute left-0 -bottom-0.5 w-full h-0.5 bg-pink-600 scale-x-0
                    group-hover:scale-x-100 transition-transform origin-left"></span>
                 </span>
                 <Icon icon="weui:arrow-outlined" 
                 class="w-5 h-5 transition-transform group-hover:translate-x-1"></Icon>
                </a>
            </article>
        </li>
      </ul>
     </div>
    </section>
</template>