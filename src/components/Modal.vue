<template>
  <slot name="body">default body</slot>
    <div v-if="isShown" class="modal">
      <div class="modal-content">
        <span class="close">&times;</span>
        <h2>Test1</h2>
        <p>Some text in the Modal..</p>
        <button @click="$emit('close')" >Close</button>
      </div>
    </div>
    
</template>

<script>
export default {
  props:{
    isShown : Boolean
  }
};
</script>

<style scoped>

.modal {
  display: none; 
  position: fixed; 
  z-index: 1; 
  left: 0;
  top: 0;
  width: 100%; 
  height: 100%; 
  overflow: auto; 
  background-color: rgb(0,0,0); 
  background-color: rgba(0,0,0,0.4); 
}

.modal-content {
  background-color: #fefefe;
  margin: 15% auto; 
  padding: 20px;
  border: 1px solid #888;
  width: 80%; 
}
</style>