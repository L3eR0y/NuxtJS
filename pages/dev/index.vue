<template lang="pug">
  div
    span {{fullName}}
    span {{message}}
</template>

<script lang="ts">
import Vue from 'vue'
import {
  Component, Prop, Watch, Lifecycle, p
} from 'av-ts'

@Component()
export default class App extends Vue {
  user_name:string = 'VOVA'
  message:string = 'This is message'

  @Lifecycle
  created () {
    console.log('CREATED')
  }

  @Lifecycle
  mounted () {
    console.log('MOUNTED')
  }

  get fullName():string{
    return 'VOVA CHUMA '
  }
}
</script>