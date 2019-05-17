<template>
  <div>
    <p>
      <TaskInput label="first" />
    </p>
    <p>
      <TaskInput label="second" />
    </p>
    <p>
      <button @click="send">Send!</button>
    </p>
  </div>
</template>

<script>
import TaskInput from "@/components/TaskInput";

export default {
  components: { TaskInput },
  data() {
    return {};
  },
  methods: {
    async send() {
      let valid = await this.$validator.validate();
      alert(valid);
    }
  }
};
</script>
