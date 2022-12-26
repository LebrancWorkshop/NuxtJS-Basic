<template>
  <div>
    <v-form>
      <v-text-field v-model="name" label="name"></v-text-field>
      <v-text-field v-model="price" label="price"></v-text-field>
      <v-btn @click="submitLog">Submit</v-btn>
    </v-form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: "",
        price: ""
      }
    },
    methods: {
      submitLog() {
        console.log(`Name: ${this.name}\nPrice: ${this.price}`)
      }
    }
  }
</script>

<style lang="css" scoped>

</style>
