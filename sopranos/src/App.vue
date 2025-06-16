<script>
import BaseCounter from './components/BaseCounter.vue'

export default {
  components: {
    BaseCounter,
  },
  data() {
    return {
      newCharacter: { name: '' },
      listOfCharacters: [
        { name: 'Tony', role: 'Boss' },
        { name: 'Carm', role: "Tony's Wife" },
        { name: 'Paulie', role: 'Cappo' },
        { name: 'Meadow', role: "Tony's Daughter" },
        { name: 'Chris', role: 'Cappo' },
        { name: 'Adrianna', role: "Chris' Girlfriend" },
        { name: 'Furio', role: 'Henchman' },
        { name: 'Jennifer Melfi', role: 'Therapist' },
      ],
    }
  },
}
</script>

<template>
  <Counter />
  <hr />
  <ul v-for="(item, index) in listOfCharacters" :key="`item-${index}`">
    <li>Name: {{ item.name }} / Role: {{ item.role }}</li>
  </ul>
</template>
