<script setup>
import InputLabel from '@/Components/InputLabel.vue';

import TextInput from '@/Components/TextInput.vue';


defineProps({
    name:'',
    type:'text',
   
});



</script>


<template>
   <div>
       <InputLabel :for="name" :value="name" />
            <TextInput
                    :id="name"
                    :name="name"
                    
                    
                    class="mt-1 block w-full"
                   :type="type"
                    :placeholder="name"
                />

      
        
    </div>
        
    
</template>