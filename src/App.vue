<template>
  <div class="container">
    <h1>Phones App</h1>
    <PhonesTable @change-phone="finalChange" :phones="phones" />
  </div>
</template>
<script>
import PhonesTable from './components/PhonesTable.vue';


export default {
    data() {
        return {
            phones: [
                {
                    id: 1,
                    brand: "Apple",
                    name: "iPhone 14",
                    price: 999,
                    available: true
                },
                {
                    id: 2,
                    brand: "Samsung",
                    name: "Galaxy S21",
                    price: 799,
                    available: true
                },
                {
                    id: 3,
                    brand: "Google",
                    name: "Pixel 7",
                    price: 699,
                    available: false
                },
                {
                    id: 4,
                    brand: "OnePlus",
                    name: "OnePlus 9",
                    price: 729,
                    available: true
                },
                {
                    id: 5,
                    brand: "Xiaomi",
                    name: "Mi 11",
                    price: 649,
                    available: false
                },
                {
                    id: 6,
                    brand: "Sony",
                    name: "Xperia 5 III",
                    price: 899,
                    available: true
                },
                {
                    id: 7,
                    brand: "LG",
                    name: "Wing",
                    price: 999,
                    available: false
                },
                {
                    id: 8,
                    brand: "Nokia",
                    name: "8.3 5G",
                    price: 599,
                    available: true
                },
                {
                    id: 9,
                    brand: "Motorola",
                    name: "Edge Plus",
                    price: 799,
                    available: true
                },
                {
                    id: 10,
                    brand: "Huawei",
                    name: "P40 Pro",
                    price: 899,
                    available: false
                }
            ]
        };
    },
    components: { PhonesTable },
    methods : {
        finalChange(id){
            let currentPhone = this.phones.find(phone => phone.id === id)
            currentPhone.available = false   
        }
    }
}
</script>
<style>
  
</style>