<template>
  <header>
    <h1>{{ propsdata }}</h1>
    <button v-on:click="sendEvent">send</button> <!-- App.vue에 emit 보내기 -->
  </header>
</template>

<script>
import App from '../App.vue';

export default {
  props: ['propsdata'],
  methods: {
    sendEvent: function() {
      this.$emit('renew');  // renew 내용이 App.vue로 전달
    }
  }
}
</script>

<style>

</style>
