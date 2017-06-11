<template>
  <div id="app" style="text-align: center; padding: 10vw; max-width: 960px; width: 90vw">
    <div>
      <NumberInputSpinner />
    </div>
  </div>
</template>

<script>
import NumberInputSpinner from 'components/NumberInputSpinner.vue';

export default {
    components: {
        NumberInputSpinner,
    },
};
</script>
