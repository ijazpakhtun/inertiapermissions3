<script setup>
// import AdminLayout from '@/Layouts/admin/AdminLayout.vue'
import AdminLayout from '@/Layouts/admin/AdminLayout.vue';
import Table from "@/Components/Table/TableComponent.vue";
import TableRow from "@/Components/Table/TableRow.vue";
import TableHeaderCell from "@/Components/Table/TableHeaderCell.vue";
import TableDataCell from "@/Components/Table/TableDataCell.vue";
import { Head, Link, useForm, } from '@inertiajs/vue3';
import LinkPill from '@/Components/Buttons/LinkPill.vue';
import ButtonPill from '@/Components/Buttons/ButtonPill.vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import Input from '@/Components/Input.vue';
import InputError from '@/Components/InputError.vue';
import InputLabel from '@/Components/InputLabel.vue';
import TextInput from '@/Components/TextInput.vue';


const form =useForm({

    name: '',
    type:'text',
});


</script>

<template>
  
        
        <Head title="Create new Role"  />
     <AdminLayout>
     
      <div class="relative flex-auto clear-both">

        <div class="flex justify-between">
               <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight text-gray-900 md:text-4xl lg:text-4xl ml-5 mt-5 dark:text-white">Create A New Role</h1>
                
                <div class="px-2 py-5">
                    <LinkPill :href="route('roles.index')" >Back</LinkPill>
                </div>
                

        </div>
        

        <div class=" mt-6 mx-auto  px-8 py-4 bg-gray-100 shadow-md overflow-hidden sm:rounded-lg w-3/4 " >
           
           
            <form @submit.prevent="form.post(route('roles.store'))" method="post">
            
                    <!-- <Input name="name"  v-model="form.name" /> -->

             <div>
                <InputLabel for="name" value="Name" />
                <TextInput
                    id="name"
                    v-model="form.name"
                    type="name"
                    class="mt-1 block w-full"
                    
                    autofocus
                    autocomplete="name"
                   />
                  <InputError class="mt-2" :message="form.errors.name" />
                </div>

                   
                    

                    <div class="flex items-center justify-end mt-4">
            
                     <PrimaryButton class="ml-4" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                         Log in
                        </PrimaryButton>
                     </div>

                     
                    
            </form>
        </div>

    </div>
     </AdminLayout>
     


 

</template>
