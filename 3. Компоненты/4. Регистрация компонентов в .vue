// main.js
import Vue from 'vue';
import App from './App.vue';
// Глобальная регистрация
// import Car from './Car.vue';

// Vue.component('app-car', Car);

new Vue({
  el: '#app',
  render: h => h(App)
})

// App.vue
<template>
  <div>
    <h1>{{ msg }}</h1>
    
    <app-car></app-car>
  </div>
</template>

<script>
  // Локальная регистрация
  import Car from './Car.vue';

  export default {
    data () {
      return {
        msg: 'Welcome'
      }
    },
    components: {
      appCar: Car
    }
  }
</script>

<style lang="scss">

</style>

// Car.vue
<template>
    <div>
        <h3>Name: {{ carName }}</h3>
        <p>Year: {{ carYear }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                carName: 'Ford Focus',
                carYear: 2015
            }
        }
    }
</script>
