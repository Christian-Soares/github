<script setup lang="ts">
import { UForm, UFormGroup, UInput, UButton } from '#components';
import { reactive } from 'vue';

const form = reactive({
    email: '',
    senha: ''
})

const styleClasses: Record<string, string> = {
  button: "mt-3 bg-indigo-500 hover:bg-indigo-600 text-white font-bold py-3 px-6 rounded justify-center w-[100%]"
}

</script>

<template>
    <div class="bg-gradient-to-br from-indigo-500 to-pink-500 h-screen flex items-center justify-center">
        <div class="bg-neutral-100 p-10 rounded h-[70%] w-[60%] flex overflow-hidden">
            <UForm :state="form" class="flex flex-row w-full h-full">  
                <div class="flex-1 flex items-center justify-center w-full h-full">
                    <img src="../assets/images/logo.png" alt="Logo Project One" class="w-[60%] object-cover">
                </div>
                <div class="flex-1 flex flex-col w-full h-full p-8 justify-center">         
                    <div class="flex flex-col w-full h-full justify-center gap-2">  
                        <h1 class="text-black text-3xl font-bold text-center pb-8">Login</h1>
                            
                        <UFormGroup>
                            <UInput 
                                v-model="form.email" 
                                input-class="bg-neutral-100"
                                size="lg"
                                placeholder="Email" 
                                type="email"
                            />
                        </UFormGroup>
                        <UFormGroup>
                            <UInput 
                                v-model="form.senha"
                                input-class="bg-neutral-100" 
                                size="lg"
                                placeholder="Senha" 
                                type="password"
                            />
                        </UFormGroup>
                        
                        <div class="justify-center">
                            <UButton 
                            class="mt-3 bg-indigo-500 hover:bg-indigo-600 text-white font-bold py-3 px-6 rounded-full justify-center w-[100%]">
                                Entrar
                            </UButton>
                            <UButton 
                            class="mt-3 bg-pink-500 hover:bg-indigo-600 text-white font-bold py-3 px-6 rounded-full justify-center w-[100%]">
                                Registrar-se
                            </UButton>
                        </div>
                    </div>
                </div>
            </UForm>
        </div>
    </div>
</template>