<script setup>
// import AdminLayout from '@/Layouts/admin/AdminLayout.vue'
import AdminLayout from '@/Layouts/admin/AdminLayout.vue';
import Table from "@/Components/Table/TableComponent.vue";
import TableRow from "@/Components/Table/TableRow.vue";
import TableHeaderCell from "@/Components/Table/TableHeaderCell.vue";
import TableDataCell from "@/Components/Table/TableDataCell.vue";
import { Head, Link, } from '@inertiajs/vue3';
import LinkPill from '@/Components/Buttons/LinkPill.vue';



defineProps(['roles'])

</script>

<template>
  
        <!-- <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Admin
            </h2>
        </template> -->
        <Head title="Roles" id="roles" />
     <AdminLayout>
     
      <div class="relative flex-auto clear-both">

        <div class="flex justify-between">
               <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-4xl lg:text-4xl ml-5 mt-5 dark:text-white"> Roles</h1>
                
                <div class="px-2 py-5">
                    <LinkPill :href="route('roles.create')" >Create Role</LinkPill>
                </div>
                

        </div>
        <Table  >
         
            <template   #header>
            
             <TableRow>
                <TableHeaderCell>ID</TableHeaderCell>
                <TableHeaderCell>Name</TableHeaderCell>
             
                <TableHeaderCell>Action</TableHeaderCell>
             </TableRow>
            
            </template>

            <template #default>
                <TableRow v-for="role in roles" :key="role.id">
                    <TableDataCell>{{ role.id }}</TableDataCell>
                    <TableDataCell>{{ role.name }}</TableDataCell>
                    <TableDataCell>Edit/Delete</TableDataCell>
                </TableRow>
            </template>




        </Table>

    </div>
     </AdminLayout>
     


 

</template>
