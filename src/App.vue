<template>
  <div>
    <router-view></router-view>
    <div class="todos-container">
      <p>Todos From Vuex:</p>
      <ul>
        <li v-for="todo in todos" :key="todo">{{ todo }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  computed: {
    ...mapGetters(["todos"]),
  },
};
</script>

<style lang="scss" scoped>
.todos-container {
  margin-top: 30px;
}
</style>
