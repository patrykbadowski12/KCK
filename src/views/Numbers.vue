<template>
  <v-container fluid class="text-xs-center">
    <v-btn outline round color="black" class="hidden-md-and-down " @click="changeNumber()">Losuj</v-btn>
     <router-link to="/" tag="btn">
            <v-btn flat>Numbers</v-btn>
        </router-link>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      randnum: null
    };
  },
  methods: {
    changeNumber: function() {
      this.randnum = Math.floor(Math.random() * 200);
    }
  },
  watch: {
    randnum: function(newValue, oldValue) {
      console.log("Poprzednia wartość " + oldValue, "Aktualna wartość " + newValue);
    }
  }
};
</script>