<template>
    <li>
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRUZqBJbCPFbsbmWd0nGOWmKV-aAgRwYylKWw&s">
      <hr>
      <slot name="card-header"></slot>
      <slot name="card-button"></slot>
      <slot name="card-content"></slot>
    </li>
</template>

<script>
export default {

}
</script>

<style scoped>
li {
  margin: 1rem 0;
  font-size: 1.25rem;
  font-weight: bold;
  background-color: purple;
  padding: 0.5rem;
  color: white;
  border-radius: 25px;
  transition: all 0.3s;
}

li:hover {
  background-color: rgb(113, 4, 113);
}

img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
}
</style>