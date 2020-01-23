<template>
    <div id="app" style="text-align: center; padding: 10vw; max-width: 960px; width: 90vw">
        <div>
            <!-- <NumberInputSpinner /> -->
            <hr>
            <number-input-spinner :integerOnly="false" value='10' :max="1000" v-model="row.value"/>

            <input type="number" v-model="row.value">
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
        row: {
          value: 10
        },
      };
    },
  };
</script>
