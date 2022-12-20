<template>
  <div class="about">
    <h1>This is an about page</h1>
    <TextInputVue :input="input" @input-event="getValue"/>
  </div>
</template>

<script>
import TextInputVue from '../components/dataentry/TextInput.vue';

export default {
  components: {
  TextInputVue
},
data() {
  return {
    input: ''
  }
},
methods: {
  getValue(valueReceived) {
    this.input = valueReceived
    console.log(valueReceived)
  }
}
}
</script>