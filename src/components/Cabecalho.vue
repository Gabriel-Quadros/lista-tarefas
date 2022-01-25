<template>
  <header>
      <h1>{{ valor }}</h1>
  </header>
</template>

<script>
export default {
  props :["valor"],
};
</script>

<style scoped>
header {
  background-color: rgb(30, 39, 66);
  height: 50px;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
}

h1 {
  color: aliceblue;
}

</style>