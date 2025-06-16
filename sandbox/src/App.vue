<script>
export default {
  data() {
          return {
            message: "Hello it works",
            newCharacter: { name: "" },
            listOfCharacters: [
              { name: "Appa" },
              { name: "Aang" },
              { name: "Zuko" },
            ],
            count: 0,
            incrementAmount: 8,
          };
        },
        methods: {
          incrementCount() {
            this.count += this.incrementAmount;
          }
        },
        watch: {
          count(newValue) {
            console.log("newVaue: ", newValue);
          }
        }
}
</script>

<template>
    <ul v-for="(item, index) in listOfCharacters" :key="`item-${index}`">
      <li>{{ item.name }}</li>
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
