<template>
  <button @click="onClick"><slot /></button>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup(_props, context) {
    const onClick = () => {
      context.emit('click')
    }
    return {
      onClick,
    }
  },
})
</script>
