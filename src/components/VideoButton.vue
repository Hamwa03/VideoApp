<template>
  <button
    type="button"
    class="rounded-md text-white bg-slate-700 hover:bg-opacity-30 p-2 text-sm font-medium"
  >
    {{ buttonText }}
  </button>
</template>

<script>
export default {
  props: {
    buttonText: String,
  },
};
</script>
