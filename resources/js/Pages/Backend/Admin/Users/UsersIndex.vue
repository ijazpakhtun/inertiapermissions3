<script setup>
// import AdminLayout from '@/Layouts/admin/AdminLayout.vue'
import AdminLayout from '@/Layouts/admin/AdminLayout.vue';
import Table from "@/Components/Table/TableComponent.vue";
import TableRow from "@/Components/Table/TableRow.vue";
import TableHeaderCell from "@/Components/Table/TableHeaderCell.vue";
import TableDataCell from "@/Components/Table/TableDataCell.vue";

defineProps(['users'])

</script>

<template>
  
        <!-- <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Admin
            </h2>
        </template> -->

     <AdminLayout>
     
      <div class="relative flex-auto clear-both">
        <span><h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-4xl lg:text-4xl ml-5 mt-5 dark:text-white"> Users</h1></span>
        <Table  >
         
            <template   #header>
            
             <TableRow>
                <TableHeaderCell>ID</TableHeaderCell>
                <TableHeaderCell>Name</TableHeaderCell>
                <TableHeaderCell>Email</TableHeaderCell>
                <TableHeaderCell>Status</TableHeaderCell>
                <TableHeaderCell>Action</TableHeaderCell>
             </TableRow>
            
            </template>

            <template #default>
                <TableRow v-for="user in users" :key="user.id">
                    <TableDataCell>{{ user.id }}</TableDataCell>
                    <TableDataCell>{{ user.name }}</TableDataCell>
                    <TableDataCell>{{ user.email }}</TableDataCell>
                    <TableDataCell>online/offline</TableDataCell>
                    <TableDataCell>Edit/Delete</TableDataCell>
                </TableRow>
            </template>




        </Table>

    </div>
     </AdminLayout>
     


 

</template>
