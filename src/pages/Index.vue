<template>
  <Layout>
    <section class="d-flex">
      <v-container>
        <v-row>
          <v-col sm="6">
            <g-image alt="Example image" src="~/slika.jpg" width="400" />
          </v-col>
          <v-col sm="6">
            <h1>Hi, I'm Ivana</h1>
            <p>I'm software developer...</p>
          </v-col>
        </v-row>
      </v-container>
    </section>


  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
