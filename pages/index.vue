<template lang="pug">
div(style="height:100vh")
  v-container.gray.lighten-5.fill-height
    v-row
      v-col(cols="3")
        v-row
          v-col
            v-card.outlined.tile 
              nuxt-link(to="/") Start
        v-row(v-for="(row,index) in 5" :key="index")
          v-col
            v-card.outlined.tile 
              nuxt-link(:to="'/' + index") Column number {{index}}
      v-col(cols="9" style="border:1px black solid")
        nuxt-child(:key="$route.params.id")
</template>

<script lang="ts">
import Vue from 'vue'
import {
  Component, Prop, Watch, Lifecycle, p
} from 'av-ts'

@Component()
export default class extends Vue {
  onRowClick(index:number){
    this.$router.push({
      name: 'dev'
    })
    
  }
}
</script>