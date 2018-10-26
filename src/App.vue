<template>
  <div id="app" style="text-align: center; padding: 10vw; max-width: 960px; width: 90vw">
    <div>
      <!-- <NumberInputSpinner /> -->
      <hr>
      <NumberInputSpinner :integerOnly="false"  value='10' :max="1000" v-model="test"/>
    </div>
  </div>
</template>

<script>
import NumberInputSpinner from 'components/NumberInputSpinner.vue';

export default {
    components: {
        NumberInputSpinner,
    },

    data: function () {
        return {
            test: 10,
        };
    },
};
</script>
