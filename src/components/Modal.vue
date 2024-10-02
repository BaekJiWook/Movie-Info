<template>
    <div class="modal">
      <div class="inner">
        <h3>{{ data[selectedMovie].title }}</h3>
        <p>영화 상세정보</p>
        <!-- <button @click="isModal = false">닫기</button> -->
        <!-- props로 전달받은 데이터는 자식이 변경못해_부모만 변경가능
         즉, App컴포넌트에서만 변경가능 -->
        <button @click="$emit('closeModal')">닫기</button>
        <!-- $emit('이벤트명')_부모는 모달을 닫아달라는 이벤트를 전달받게돼  -->
     
      </div>
    </div>
  </template>
    
  <script>
  export default {
    name: "ModalComponent",
    // app에서 보낸 것을 받아야함 props로
    props {
      data: Array,
      isModal: Boolean,
      selectedMovie: Number,
    }
  }
  
  </script>
    
  <style></style>