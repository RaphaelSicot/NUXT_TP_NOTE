<template>
  <div>
    <li v-for="planet in filterAstre" :key="planet.id">
      {{ planet.name }}
    </li>
  </div>
</template>

<script>
export default {
  layout: "default",
  data() {
    return {
      planets: [],
    };
  },
  async mounted() {
    const response = await this.storePlanets();
    this.planets = response;
    // eslint-disable-next-line no-console
    console.log(this.planets);
  },
  methods: {
    storePlanets() {
      return this.$axios
        .$get("https://api.le-systeme-solaire.net/rest/bodies/")
        .then((Response) => {
          return Response.bodies;
        });
    },
  },
  computed: {
    filterAstre() {
      if (this.IsPlanet && this.HasMoons) {
        return this.astres
          .filter((astre) => astre.isPlanet === true)
          .filter((astre) => astre.moons !== null);
      }
      if (this.HasMoons) {
        return this.astres.filter((astre) => astre.moons !== null);
      }
      if (this.IsPlanet) {
        return this.astres.filter((astre) => astre.isPlanet === true);
      }

      return this.astres;
    },
  },
};
</script>

