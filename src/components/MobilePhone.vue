<template>
    <tr>
        <td>{{ phone.id }}</td>
        <td>{{ phone.brand }}</td>
        <td>{{ phone.name }}</td>
        <td>{{ phone.price }}</td>
        <td v-if="phone.available"><i @click="makePhoneUnavailable" class="bi bi-bag-check text-success"></i></td>
        <td v-else><i class="bi bi-bag-x text-danger"></i></td>
    </tr>
</template>
<script>
export default {
    props : {
        phone : {
            type : Object,
            required : true
        }
    },
    emits : ['my-event'],
    methods : {
        makePhoneUnavailable() {
            this.$emit('my-event', this.phone.id)
        }
    }
}
</script>
<style lang="">
    
</style>