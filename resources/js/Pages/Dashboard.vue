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
                Dashboard
            </h2>
        </template>

     
      
         <!-- Main layout -->
  <div class="flex flex-col md:flex-row">
    <!-- Sidebar -->
    
    <Sidebar ></Sidebar>
    <!-- Main content section -->
    
        <div class="max-w-7xl mx-auto sm:px-6 lg:px-8 mt-5">
                <div class=" overflow-hidden shadow-xl sm:rounded-lg mb-5">
                    <Welcome />
                </div>
            </div>
   
  </div>


  <Footer class="flex flex-col md:flex-row"></Footer>

    </AppLayout>
</template>
