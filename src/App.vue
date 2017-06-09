<template>
  <div id="app" style="text-align: center; padding: 10vw">
    <div>
      <NumberInputSpinner
        :max="10"
        :min="-10"
      />
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
