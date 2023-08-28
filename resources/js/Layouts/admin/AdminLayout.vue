<script setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import Welcome from '@/Components/Welcome.vue';
import Sidebar from '@/Layouts/admin/layout/Sidebar.vue';
import Footer from '@/Layouts/admin/layout/Footer.vue';

</script>

<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Admin
            </h2>
        </template>

     
      
         <!-- Main layout -->
  <div class="flex flex-col md:flex-row">
    <!-- Sidebar -->
    
    <Sidebar ></Sidebar>
    <!-- Main content section -->
    
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-10  w-full mb-5">
                <div class=" overflow-hidden shadow-xl sm:rounded-lg   min-h-full  ">

                    <!-- <Head title="Welcome" /> -->

                    <div class="relative sm:flex sm:justify-center mt-6  h-screen w-fill sm:rounded-lg  bg-dots-darker bg-center bg-white dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white ">
                      
                       <slot></slot>
                       
                        

                    </div>
                 
                </div>
            </div>
   
  </div>


  <Footer class="flex flex-col md:flex-row"></Footer>

    </AppLayout>
</template>


<style>
.bg-dots-darker {
    background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(0,0,0,0.07)'/%3E%3C/svg%3E");
}
@media (prefers-color-scheme: dark) {
    .dark\:bg-dots-lighter {
        background-image: url("data:image/svg+xml,%3Csvg width='30' height='30' viewBox='0 0 30 30' fill='none' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M1.22676 0C1.91374 0 2.45351 0.539773 2.45351 1.22676C2.45351 1.91374 1.91374 2.45351 1.22676 2.45351C0.539773 2.45351 0 1.91374 0 1.22676C0 0.539773 0.539773 0 1.22676 0Z' fill='rgba(255,255,255,0.07)'/%3E%3C/svg%3E");
    }
}
</style>
