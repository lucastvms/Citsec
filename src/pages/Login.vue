<template>
    <div class="surface-0 flex align-items-center justify-content-center min-h-screen min-w-screen overflow-hidden">
        <div class="grid justify-content-center p-2 lg:p-0" style="min-width:80%">
            <div class="col-12 mt-5 xl:mt-0 text-center">
                <img :src="'layout/images/citsec.png'" alt="Cit logo" class="mb-5" style="width:300px; height:300px;">
            </div>
            <!-- background: linear-gradient(180deg, var(--primary-color), rgba(33, 150, 243, 0) 30%); -->
            <div class="col-12 xl:col-6" style="border-radius:56px; padding:0.3rem;">
                
                <!-- border-radius:53px; background: linear-gradient(180deg, var(--surface-50) 38.9%, var(--surface-0)); -->
                <div class="h-full w-full m-0 py-7 px-4" style="box-shadow: 0px 5px 17px; rgba(34, 35, 58, 0.2); border-radius:56px; padding:0.3rem;">
                    <div class="text-center mb-5">
                        <!-- <img src="layout/images/avatar.png" alt="Image" height="50" class="mb-3"> -->
                        <!-- <div class="text-900 text-3xl font-medium mb-3">Welcome, Isabel!</div>
                        <span class="text-600 font-medium">Sign in to continue</span> -->
                    </div>
                
                    <div class="md:w-10 mx-auto">
                        <label for="email1" class="block text-900 text-xl font-medium mb-2">Usuário</label>
                        <InputText id="email1" v-model="email" type="text" class="w-full mb-3" style="padding:1rem;" />
                
                        <label for="password1" class="block text-900 font-medium text-xl mb-2">Senha</label>
                        <!-- <Password id="password1" v-model="password" :toggleMask="true" class="w-full mb-3" inputClass="w-full" inputStyle="padding:1rem"></Password> -->
                        <InputText id="password1" v-model="password" type="text" class="w-full mb-3" style="padding:1rem;" />
                
                        <div class="flex align-items-center justify-content-between mb-5">
                            <div class="flex align-items-center">
                                <Checkbox id="rememberme1" v-model="checked" :binary="true" class="mr-2"></Checkbox>
                                <label for="rememberme1">Lembre-me</label>
                            </div>
                            <a class="font-medium no-underline ml-2 text-right cursor-pointer" style="color: #3783c6">Esqueci minha senha!</a>
                        </div>
                        <!-- <Button label="Entrar" class="p-3 text-xl"></button> -->
                    </div>
                    <div style="text-align: center; justifyContent: center; display: flex;">
                        <Button label="Entrar" class="p-3 text-xl" style="width: 250px" @click="$router.push('app/dashboard')"></button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'login_page',
    data() {
        return {
            email: '',
            password: '',
            checked: false
        }
    },
    // computed: {
    //     logoColor() {
    //         if (this.$appState.darkTheme) return 'white';
    //         return 'dark';
    //     }
    // }
}
</script>

<style scoped>
.pi-eye {
    transform:scale(1.6);
    margin-right: 1rem;
}

.pi-eye-slash {
    transform:scale(1.6);
    margin-right: 1rem;
}
</style>
