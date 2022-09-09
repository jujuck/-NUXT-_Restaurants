<template>
  <div>
    <Html>
      <Head>
        <Title>Find your Restaurantly</Title>
        <Meta
          name="description"
          content="Find the best resraurantS"
        />
      </Head>
    </Html>
    <NuxtLayout name="costum">
      <div class="container">
        <RestaurantsTable />
      </div>
    </NuxtLayout>
  </div>
</template>

<style>
.container {
  text-align: center;
  margin-top: 5rem;
}
</style>
