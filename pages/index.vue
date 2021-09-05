<template>
  <div class="parent-frame">
    <iframe src="https://sharing.clickup.com/l/h/6-128546959-1/b214b8d06b3566b" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      list: null
    }
  }
}
</script>

<style scoped>

.parent-frame{
  overflow: hidden;
  height: calc(100% + 10px)
}
iframe{
  position: relative;
  border: none;
  top: -52px; width:100%;
  height: calc(100% + 52px);
  background: transparent;
}
</style>
