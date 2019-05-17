<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <TaskForm />
  </div>
</template>

<script>
import TaskForm from "@/components/TaskForm";

export default {
  name: "app",
  components: {
    TaskForm
  }
};
</script>
