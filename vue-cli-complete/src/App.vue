<template>
  <div>
    <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
     <!-- 컴포넌트 파일명은 파스칼케이스 사용, 최소 2단어 사용 권장  ex) AppHeader -->
    <app-header 
      v-bind:propsdata="str"
      v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

// var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }

// new Vue({
//   data: {
//     str: 'hi'
//   }
// })

export default {
  // 인스턴스 옵션 속성 or 컴포넌트 옵션 속성
  data: function() {
    return {
      str: 'Header!!!'  //props str 내보내기
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'hi';    //str 값을 바꾸는 emit 속성
    }
  }
}
</script>

<style>

</style>
