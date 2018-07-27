<template>
  <div class="home">
    <img src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
    <MyComponent/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import MyComponent from '@/components/MyComponent.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,MyComponent
  },
})
export default class Home extends Vue {}
</script>
