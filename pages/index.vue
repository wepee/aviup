<template>
  <div class="parent-frame">
    <div style="position: absolute; align-items: center; display: flex; top: -10px; left: calc(50% - 60px); z-index: 100000">
      <v-icon>mdi-table</v-icon>
      <h4 class="px-2">
        Tableau
      </h4>
      <v-switch v-model="tableau" style="display: inline-block" />
    </div>
    <iframe :src="tableau ? 'https://sharing.clickup.com/b/h/6-128546959-2/2970c84cf5222bf' : 'https://sharing.clickup.com/l/h/6-128546959-1/b214b8d06b3566b'" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      tableau: false
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
