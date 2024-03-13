<!-- Modal.vue -->
<template>
    <div class="modal" v-if="show">
      <div class="modal-content">
        <span class="close" @click="closeModal">&times;</span>
        <p>Added to cart. Thanks for shopping!</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const show = ref(false)
  
  function closeModal() {
    show.value = false
  }

  </script>
  
  <style scoped>
  /* Modal styles */
  .modal {
    display: none; /* Hidden by default */
    position: fixed; /* Stay in place */
    z-index: 1; /* Sit on top */
    left: 0;
    top: 0;
    width: 100%; /* Full width */
    height: 100%; /* Full height */
    overflow: auto; /* Enable scroll if needed */
    background-color: rgb(0,0,0); /* Fallback color */
    background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
  }
  
  /* Modal content */
  .modal-content {
    background-color: #fefefe;
    margin: 15% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
  }
  
  /* Close button */
  .close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
  }
  
  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }
  </style>
  