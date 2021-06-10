<template>
  <div>
    <h1>Hello {{ name }}</h1>
    <input type="text" v-model="name" />

    <br />

    <a :href="link">link para o Google</a>
  </div>
</template>

<script>
export default {
  data: () => ({
    name: "Eduardo",
    link: "https://www.google.com",
  }),
};
</script>