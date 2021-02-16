<template>
  <div>
    <my-x />
    <component :is="myComponentName" />
  </div>
</template>

<script>
import { h } from 'vue'

// 1. Notice the hydration error.
// 2. Remove <my-x /> from template above OR replace it with <div />. Notice no hydration error

export default {
  components: {
    MyX: {
      setup () {
        return () => h('div')
      }
    },

    ComponentA: {
      setup () {
        return () => h('div')
      }
    }
  },

  setup () {
    return {
      myComponentName: 'ComponentA'
    }
  }
}
</script>
