<template>
  <button
    type="button"
    class="rounded-xl text-white bg-slate-700 hover:bg-slate-600 p-2"
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
