<script>
export default {
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
      count: 0,
      incrementAmount: 1,
    }
  },
  methods: {
    incrementCount() {
      const val = typeof this.incrementAmount === 'string' ? 0 : this.incrementAmount
      this.count += val
    },
  },
}
</script>

<template>
  <h1>Keeping Track of count</h1>
  <h3>{{ count }}</h3>
  <label for="incrementAmount">Increment Amount</label>
  <input type="number" v-model.number="incrementAmount" />
  <button @click="incrementCount">Increment</button>
  <hr />
  <ul v-for="(item, index) in listOfCharacters" :key="`item-${index}`">
    <li>Name: {{ item.name }} / Role: {{ item.role }}</li>
  </ul>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
