<template>
  <div>
    <h1>{{ message }}</h1>
    <h2>hi</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: ''
    };
  },
  mounted() {
    fetch('http://localhost:3000/api/data')
      .then(response => response.json())
      .then(data => {
        this.message = data.message;
      })
      .catch(error => {
        console.error('Error fetching data:', error);
      });
  }
};
</script>

<style scoped>
h1 {
  color: #42b983;
}
</style>