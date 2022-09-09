<template>
  <div class="table">
    <h1>TOP 50: THE RANKING</h1>
    <div class="table-container">
      <div class="table-col">
        <RestaurantsRow :isHeader="true" />
        <RestaurantsRow 
          v-for="(resto, index) in restaurantsOrganized.first" 
          :key="resto.id" 
          :name="resto.name"
          :rank="resto.rank"
          :index="index"
        />
      </div>
      <div class="table-col">
        <RestaurantsRow :isHeader="true" />
        <RestaurantsRow 
          v-for="(resto, index) in restaurantsOrganized.second" 
          :key="resto.id"
          :name="resto.name"
          :rank="resto.rank"
          :index="index"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import restaurants from '@/data.json';

  const restaurantsOrganized = {
    first: [...restaurants.splice(0,25)],
    second: [...restaurants.splice(0, 25)]
  }
  console.log(restaurantsOrganized)
</script>

<style scoped>
.table {
  margin: 3rem 0;
}
.table h1 {
  margin-bottom: 2rem;
}
.table-container {
  display: flex;
  justify-content: space-between;
}
.table-col {
  width: 48%;
}

</style>