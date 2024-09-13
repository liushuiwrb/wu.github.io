<template>
  <div class="App">
    <div class="appos">
      <h3>Welcome to Your Vue App</h3>
    </div>
    <p v-for="nas in actel" :key="nas.id">{{ nas.name }} -- {{ nas.age }}</p>

  </div>
  <Person :liushui="actel"/>
</template>


<script lang="ts" setup name="App">
    import { reactive } from "vue";
    import Person from "./components/Person.vue";

    // 定义数据
    let actel = reactive([
      {id: 1, name: "张三", age: 20 },
      {id: 2, name: "李四", age: 25 },
      {id: 3, name: "王五", age: 30 },
      {id: 4, name: "赵六", age: 35 },
    ])

    // 定义方法


    


</script>

<style scoped>
    .App{
      border: 1px solid black;
      margin: 20px auto;
    }
</style>