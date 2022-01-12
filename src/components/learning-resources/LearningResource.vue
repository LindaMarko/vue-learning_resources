<template>
  <li>
    <base-card>
      <header>
        <h3>{{ title }}</h3>
        <base-button mode="flat" @click="deleteResource(id)"
          >Delete</base-button
        >
      </header>
      <p>{{ description }}</p>
      <nav>
        <a :href="link">View Resource</a>
      </nav>
    </base-card>
  </li>
</template>

<script>
export default {
  inject: ['deleteResource'],
  props: ['id', 'title', 'description', 'link'],
};
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-family: 'Open Sans', sans-serif;
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  font-weight: 700;
  text-decoration: none;
  color: #c5038b;
}

a:hover,
a:active {
  color: #80006e;
}
</style>
