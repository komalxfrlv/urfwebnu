<template>
  <section class="app">
    <NavigationComponent/>
    <section class="page">
      <NuxtPage />
    </section>
    <FooterComponent/>
  </section>
</template>
<style>
* {
  margin: 0;
  padding: 0;
}
.page {
  padding-top: 88px;
}
a {
  text-decoration: none;
}

li {
  list-style: none;
}
</style>
