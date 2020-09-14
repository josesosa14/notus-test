<template>
    <div class="vld-parent">
        <loading :active.sync="isLoading" 
        :can-cancel="true" 
        :on-cancel="onCancel"
        :background-color="backgroundColor"
        :opacity="opacity"
        :is-full-page="fullPage">
        <img src="../assets/img/Notus-logo-loading.svg" class="logo-loading"/>
        </loading>
        
    </div>
</template>
 
<script>
    // Import component
    import Loading from 'vue-loading-overlay';
    // Import stylesheet
    import 'vue-loading-overlay/dist/vue-loading.css';
    
    export default {
        created(){
            setTimeout(() => {
                this.isLoading = false
            },3000)
        },
        data() {
            return {
                isLoading: true,
                fullPage: true,
                backgroundColor: "#081B2F" ,
                opacity: 0.9,
            }
        },
        components: {
            Loading
        },
        methods: {
            onCancel() {
              console.log('User cancelled the loader.')
            }
        }
    }
</script> 
<style scoped>
    .logo-loading:hover{
        -webkit-transform: rotate(360deg);transform: rotate(360deg);
    }
</style>