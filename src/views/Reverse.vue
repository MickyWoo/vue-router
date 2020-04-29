<template>
  <div class="reverse">
    <h1>This is a reverse page</h1>

    <h2> please enter a string to reverse!</h2>
    <label> String:
      <input type="text" id="string" v-model="message">
      </label>
      <h2> the reverse message is:  </h2>
      <p> {{ reverseMessage}} </p>
  </div>
</template>

<script>
export default {
  name: 'reverse',
  data() {
    return {
      message: 'hello'
    }
  },
  computed: {
    reverseMessage() {
      return this.message.split('').reverse().join('');
    }
  }
}
</script>