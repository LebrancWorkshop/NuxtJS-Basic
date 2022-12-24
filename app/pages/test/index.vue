<template>
  <div>
    <h2 v-if="isMessageShow">{{ message }}</h2>
    <h2 v-else>{{ errorMessage }}</h2>
    <v-btn @click="changeStatus">
      Change Status
    </v-btn>
    <h3>
      Member:
      <p v-for="(member, index) in members" :key="index">
        {{ member }}
      </p>
    </h3>
    <h3>
      Instant Message: {{ instantMessage }}
      <v-text-field v-model="instantMessage"></v-text-field>
    </h3>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        message: "Ikigai",
        errorMessage: "Unknown Data",
        isMessageShow: false,
        members: [
          "Jan",
          "SomSom",
          "Mint"
        ],
        instantMessage: "Hello World"
      }
    },
    methods: {
      changeStatus() {
        this.isMessageShow = !this.isMessageShow;
      }
    }
  }
</script>

<style>

</style>
