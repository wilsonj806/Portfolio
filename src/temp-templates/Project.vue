<template>
  <Layout>
    <!-- Figure out how to make this a component instead -->
    <div class="project" v-html="$page.project.content"/>
    <g-image :src="$page.project.image"/>
  </Layout>
</template>
<script>
export default {
  name: 'Project'
}
</script>

<page-query>
query Project($id: ID!) {
  project(id:$id) {
    id
    path
    content
  }
}
</page-query>

<style scoped>
.project {
  margin: auto;
  max-width: 65%;
}
</style>