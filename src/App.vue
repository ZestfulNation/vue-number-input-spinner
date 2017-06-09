<template>
  <div id="app">
    <a href="https://github.com/krystalcampioni/vue-number-input-spinner">
      <img style="position: absolute; top: 0; right: 0; border: 0;" src="https://camo.githubusercontent.com/38ef81f8aca64bb9a64448d0d70f1308ef5341ab/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f6461726b626c75655f3132313632312e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_darkblue_121621.png">
    </a>
    <header class="header">
      <div class="grid">
        <h1>Vue Number Input Spinner</h1>
      </div>
    </header>
    <div>
    <div class="grid">
      <div class="grid__full">
        <h2>A customizable number input spinner component for Vuejs</h2>
      </div>

      <div class="grid__half">
        <p>Install the package via NPM and import it in your project:</p>
        <pre v-highlightjs>
          <code class="javascript">
            {{ this.snippet1 }}
        </code>
      </pre>

      <pre v-highlightjs>
        <code class="javascript">
          {{ this.snippet2 }}
      </code>
    </pre>

      </div>
      <div class="grid__half">
        <NumberInputSpinner
          :max="10"
          :min="-10"
        />
      </div>
    </div>
    </div>
  </div>
</template>

<script>

import NumberInputSpinner from 'components/NumberInputSpinner.vue';

export default {
    components: {
        NumberInputSpinner,
    },
    data() {
        return {
          snippet1:
            `
            import NumberInputSpinner from 'vue-number-input-spinner'

            export default {
              components: {
                NumberInputSpinner,
              },
            }`,

          snippet2: `<NumberInputSpinner
            :min="0"
            :max="10"
            :inputClass="your-css-class"
            :buttonClass="your-other-css-class"
            :integerOnly="true"
            @newNumber="someFunction"
          />`
        }
    }

};
</script>

<style lang="scss">
  html,
  body {
    margin: 0;
    padding: 0;
    font-family: sans-serif;
  }

  h1, h2 { display: inline-block; }

  h2 {
    font-weight: lighter;
    color: #387e90;
  }

  pre {
    margin: 0;
    padding: 0;
  }

  .header {
    background: linear-gradient(141deg, #0fb8ad 0%, #1fc8db 51%, #2cb5e8 75%);
    color: #fff;
    padding: 20px;
    width: 100%;
    float: left;
  }

  .grid {
    width: 90vw;
    max-width: 1200px;
    margin: 0 auto;

    &__full {
      margin: 0 20px 20px;
      width: 100%;
      float: left;
    }

    &__half {
      width: calc(50% - 40px);
      margin: 0 20px 20px ;
      float: left;
    }
  }

</style>
