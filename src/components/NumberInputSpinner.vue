<template>
  <div class="vnis" >
    <input type="button" @click="decreaseNumber" class="vnis__button" value="-"/>
    <input
        v-model.number="numericValue"
        @keypress="isNumber"
        class="vnis__field form__input"
        type="number"
        :min="min"
        :max="max"
        debounce="500"
    />
    <input type="button" @click="increaseNumber" class="vnis__button" value="+"/>
  </div>
</template>

<script>
export default {
    name: 'NumberInputSpinner',

    data: function () {
        return {
            numericValue: 0,
        };
    },

    props: {
        min: {
            default: 0,
            type: Number
        },
        max: {
            default: 100,
            type: Number
        }
    },

    methods: {
        increaseNumber() { this.numericValue++; },

        decreaseNumber() { this.numericValue--; },

        isNumber(evt) {
            evt = (evt) ? evt : window.event;
            let key = evt.keyCode || evt.which;
            key = String.fromCharCode( key );
            const regex = /[0-9]/;

            if( !regex.test(key) ) {
                evt.returnValue = false;
                if(evt.preventDefault) evt.preventDefault();
            }
        }
    },

    watch: {
        numericValue: function(val, oldVal){
            if(val <= 0) { this.numericValue = 0; }

            if(val >= this.max) { this.numericValue = parseInt(this.max); }

            if(val <= this.max) {
                this.$emit('newNumber', val, oldVal );
            }
        }
    }
};
</script>

<style lang="scss" scoped>
 input {
   &[type='number'] {
     -moz-appearance: textfield;
   }

 &::-webkit-outer-spin-button,
   &::-webkit-inner-spin-button {
     -webkit-appearance: none;
   }
 }

.vnis {
   background: red;

 &__button {
     background: green;
   }
 }
</style>
