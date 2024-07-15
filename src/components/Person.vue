<template>
  <Card>
    <template v-slot:card-header>
      <h1>{{ name }}</h1>
    </template>

    <template v-slot:card-content>
      <p>เงินเดือน: {{ salary }} บาท , เพศ : {{ gender }}</p>
      <p>ตำแหน่งงาน: {{ department }}</p>
      <p>ทักษะด้านภาษา : {{ skill }}</p>
    </template>
  </Card>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Person",
  components: {
    Card,
  },
  props: {
    name: {
      type: String,
      require: true,
    },
    salary: {
      type: Number,
      default: 25000,
    },
    department: {
      type: String,
      require: true,
    },
    gender: {
      type: String,
    },
    skill: {
      type: Array,
    }
  }
};
</script>

<style scoped>
p {
  margin-top: 10px;
}

button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  border-radius: 5px;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 2px rgba(0, 0, 0, 0.26);
  margin-top: 10px;
  transition: all 0.3s;
}

button:hover {
  background-color: #b9095b;
}

.fade-enter-from {
  opacity: 0;
}

.fade-enter-active {
  transition: all 0.5s linear;
}
</style>