<template>
  <div>
    <p>sample</p>
    <app-button @click="onClick">app-button</app-button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'
import AppButton from '~/components/AppButton.vue'

export default defineComponent({
  props: {
    test: String,
  },
  components: {
    AppButton,
  },
  setup() {
    const onClick = () => {
      console.log('clicked')
    }
    return {
      onClick,
    }
  },
})
</script>
