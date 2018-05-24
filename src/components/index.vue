<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>
      <lottie :options="defaultOptions" :height="100" :width="200" @animCreated="handleAnimation"/>
    </div>
  </div>
</template>

<script>
  import Lottie from './lottie';
  import * as animationData from './loading.json';

export default {
  components:{
    'lottie': Lottie,
  },
  data () {
    return {
      msg:'Welcome to Lottie',
      defaultOptions: {animationData: animationData},
    }
  },
  methods:{
    handleAnimation(){},
  }
}
</script>

