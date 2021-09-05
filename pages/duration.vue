<template>
  <v-container class="fill-height" style="text-align: center; width: fit-content">
    <h2 class="mr-2">
      Work in progress
    </h2>
    <v-icon>mdi-hammer-wrench</v-icon>
  </v-container>
</template>

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
