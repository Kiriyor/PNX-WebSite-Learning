<template>
  <div class="text-card">
    <h3>
      <span :class="{ [props.typcnIcon]: true }" class="typcn icon"></span>
      {{ props.title }}
    </h3>
    <p>
      {{ props.content }}
    </p>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps(["typcnIcon", "title", "content"]);
</script>

<style lang="scss" scoped>
.icon {
  padding-right: 10px;
  color: #e55d87;
}

.text-card{
  max-height: 300px;
  max-width: 375px;
  h3{
    font-size: 36px;
    font-weight: 200;
    margin-bottom: 20px;
  }
  p{
    font-size: 16px;
    letter-spacing: 1px;//文字间距
  }
}
</style>