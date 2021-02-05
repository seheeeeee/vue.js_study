<template>
  <div>
    <!-- 최상위 element는 하나만 있어야함 -->
    {{str}}
    <app-header></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
//AppHeader를 정의하고 컴포넌트를 받아옴
//= var AppHeader = {
//   template: '<header><h1>Header</h1></header>'
// }

// new Vue({
//   data: {
//     str: 'hi'
//   }
// })
export default {
  //컴포넌트 재사용을 위해 다른 컴포넌트의 data를 참조할 수 없기 때문에 객체로 저장할 수 없고 function return을 사용해야함
  data: function(){
    return{
      str: 'hi'
    }
  },
  components: {
    'app-header': AppHeader
  }
}
</script>

<style>

</style>