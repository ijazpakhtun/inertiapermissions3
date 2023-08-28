<script setup>
// import AdminLayout from '@/Layouts/admin/AdminLayout.vue'
import AdminLayout from '@/Layouts/admin/AdminLayout.vue';
import Table from "@/Components/Table/TableComponent.vue";
import TableRow from "@/Components/Table/TableRow.vue";
import TableHeaderCell from "@/Components/Table/TableHeaderCell.vue";
import TableDataCell from "@/Components/Table/TableDataCell.vue";

defineProps(['permissions'])

</script>

<template>
  
        <!-- <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Admin
            </h2>
        </template> -->

     
 <AdminLayout>
     
     <div class="relative flex-auto clear-both">
       <span><h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-4xl lg:text-4xl ml-5 mt-5 dark:text-white"> Permissions</h1></span>
       <Table v-if="permissions.length" >
      
        
           <template   #header>
           
            <TableRow>
               <TableHeaderCell>ID</TableHeaderCell>
               <TableHeaderCell>Name</TableHeaderCell>
            
               <TableHeaderCell>Action</TableHeaderCell>
            </TableRow>
           
           </template>

           <template #default>
               <TableRow v-for="permission in permissions" :key="permission.id">
                   <TableDataCell>{{ permission.id }}</TableDataCell>
                   <TableDataCell>{{ permission.name }}</TableDataCell>
                   <TableDataCell>Edit/Delete</TableDataCell>
               </TableRow>
           </template>




       </Table>

       <div v-else  class="border border-t-0 border-red-400 rounded-b bg-red-100 px-4 py-3 text-red-700">
                Permissions not found
       </div>

   </div>
    </AdminLayout>
     


 

</template>
