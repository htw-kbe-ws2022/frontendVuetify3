<template>
  <p>Counter: {{ getCounter }}</p>
  <button @click="increment(1)">
    Increment
  </button>
</template>

<script>
import {mapGetters, mapActions} from 'vuex'

export default {
  methods: {
    ...mapActions('counterModule', ['increment'])
  },
  computed: {
    ...mapGetters('counterModule', ['getCounter'])
  },

}
</script>
