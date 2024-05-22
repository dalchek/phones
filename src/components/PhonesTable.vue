<template>
    <div class="row">
        <div class="col-10 offset-1">
            <table class="table table-dark">
                <thead>
                    <tr>
                        <th>ID</th>
                        <th>Brand</th>
                        <th>Name</th>
                        <th>Price</th>
                        <th>Available</th>
                    </tr>
                </thead>
                <tbody>
                    <MobilePhone @my-event="changeAvailable" v-for="phone in phones" :phone="phone" :key="phone.id" />
                </tbody>
            </table>
        </div>
    </div>
</template>
<script>
import MobilePhone from '@/components/MobilePhone.vue';

export default {
    components: { MobilePhone },
    props : {
        phones : {
            type : Array,
            required : true
        }
    },
    emits : {
        'change-phone' : function(phoneId){}   
    },
    methods : {
        changeAvailable(id){
            this.$emit('change-phone', id)
        }
    }
}
</script>
<style>
    
</style>