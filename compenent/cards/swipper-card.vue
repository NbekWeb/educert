<template>
  <div class="card">
    <nuxt-link to="/" class="card-img df">
      <div class="card-badge top">aaaaaaaaaaaaaaaaaaaaaa</div>
      <img src="/assets/img/card.jpg" alt="" />
    </nuxt-link>
    <div class="card-body">
      <div class="rating df align-cen gap-10">
        <div class="average font-15">4.5</div>
        <cardvue :value="ratingValue" :max="5" @update:value="updateRating" />
      </div>
      <div class="context">
        <h4 class="blue-b font-18">
          Zero dan Expertgacha Intensiv Python backend dasturlash
        </h4>
        <div class="card-icons df jus-beet">
          <div class="card-icon df align-cen">
            <img src="/assets/img/icon/card/document 1.svg" alt="" />
            <p class="font-14 blue-p">16 dars</p>
          </div>
          <div class="card-icon df align-cen">
            <img src="/assets/img/icon/card/document 1.svg" alt="" />
            <p class="font-14 blue-p">16 dars</p>
          </div>
          <div class="card-icon df align-cen">
            <img src="/assets/img/icon/card/document 1.svg" alt="" />
            <p class="font-14 blue-p">16 dars</p>
          </div>
        </div>
      </div>
    </div>
    <nuxt-link to=""></nuxt-link>
  </div>
</template>
<script setup>
import { defineProps, ref } from "vue";
import cardvue from "./star.vue";

const props = defineProps(["value", "max"]);
const ratingValue = ref(3.5);

const updateRating = (newValue) => {
  ratingValue.value = newValue;
};
</script>
<style lang="scss">
@import "/assets/style/card/swipper-card.scss";
</style>
