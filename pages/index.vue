<template>
  <div>
    <Html>
      <Head>
        <Title>Restaurantly</Title>
        <Meta
          name="description"
          content="My page is so cool with nuxt JS"
        />
      </Head>
    </Html>
    <div class="container">
      <h1>Welcome to Restaurantly</h1>
      <NuxtLink href="/restaurants">Go to Restaurants</NuxtLink>
    </div>
  </div>
</template>

<style>
.container {
  text-align: center;
  margin-top: 5rem;
}
</style>
