<script setup>
import { ref, onMounted } from 'vue';
  
  // 반응적인 상태의 속성
  const count = ref(0);

  // 속성 값을 변경하고 업데이트 할 수 있는 함수.
  function increment() {
    count.value++;
  }

  // ref 이해 시작
  const roCount  = ref(2);

  function readonly() {
    console.log(roCount.value);

    roCount.value++;
  }

  // ref 이해 끝

  // 생명 주기 훅
  onMounted(() => {
    console.log(`숫자 세기의 초기값은 ${ count.value } 입니다.`);
  })

</script>


<template>
  <button @click="increment">숫자 세기: {{ count }}</button>

  <button @click="readonly">읽기 전용 숫자: {{ roCount }}</button>

  <button @click="writePossible">쓰기 가능 숫자: {{ wpCount }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
