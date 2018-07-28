<template>
  <div class="home">
    <MyComponent/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
//import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import MyComponent from '@/components/MyComponent.vue'; // @ is an alias to /src

@Component({
  components: {
    MyComponent
  },
})
export default class Home extends Vue {}
</script>
