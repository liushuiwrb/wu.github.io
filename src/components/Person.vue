<template>
    <div class="person">
        <h3>{{ name }}</h3>
        <p>{{ age }}</p>
        <p>{{ gender }}</p>
        <p>{{ occupation }}</p>
        <p v-for="item in msg" :key="item">{{ name }}</p>
        <button @click="sayHello">Say Hello</button>
        <button @click="sayGoodbye">Say Goodbye</button>
    </div>
</template>


<script lang="ts" setup name="Person">
import { ref, defineProps } from 'vue';

    let name = ref('John Doe')
    let age = ref(19)
    let gender = 'Male'
    let occupation = 'Software Engineer'
    let msg = defineProps(['liushui'])

    function sayHello() {
        name.value = 'Hello'
    }
    function sayGoodbye() {
        age.value += 1
    }
    

</script>

<style scoped>
.person {
    border: 1px solid black;
    padding: 10px;
}
</style>