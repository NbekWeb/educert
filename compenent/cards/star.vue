<template>
    <div class="star-rating">
      <span
        v-for="star in totalStars"
        :key="star"
        class="star"
        :class="{ 'filled': star <= props.value, 'half-filled': star - 0.5 === props.value }"
      >
        ★
      </span>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps(['value']);
  const totalStars = Array.from({ length: 5 }, (_, index) => index + 1);
  </script>
  
  <style lang="scss">
  .star-rating {
    display: inline-block;
  }
  
  .star {
    font-size: 1.5rem;
    color: #ccc;
    transition: color 0.3s;
  }
  
  .star.filled {
    color: #fdd835; /* Color for filled stars */
  }
  
  .star.half-filled {
    position: relative;
    display: inline-block;
  }
  
  .star.half-filled::before {
    content: '★';
    position: absolute;
    left: 0;
    width: 50%;
    overflow: hidden;
    color: #fdd835; /* Color for filled part of the half star */
  }
  
  </style>