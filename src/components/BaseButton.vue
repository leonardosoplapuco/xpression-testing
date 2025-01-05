<template>
  <div>
    <button :class="buttonStyle">
        {{ props.buttonText }}
    </button>
  </div>
</template>

<script setup lang="ts">
import { computed, PropType } from 'vue'

type ButtonType = 'primary' | 'secondary' | 'cancel'

const props = defineProps({
  buttonText: {
    type: String,
    required: false,
    default: 'Button',
  },
  buttonType: {
    type: String as PropType<ButtonType>,
    required: false,
    default: 'primary',
  },
})

const buttonStyle = computed(() => {
  const typeStyles = {
    'primary': "bg-gray-900 text-white rounded-lg",
    'secondary': "bg-white text-black rounded-lg",
    'cancel': "bg-gray-600 text-white rounded-lg",
  }
  const matchedStyle = typeStyles[props.buttonType]

  return matchedStyle
})

</script>