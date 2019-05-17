<template>
  <div>
    <h2>TASK</h2>
    <div>
      <label :for="label + '.type'">Type:</label>
      <select
        :name="label + '.type'"
        v-model="type"
        v-validate.disable="'required'"
      >
        <option value="MUST">MUST</option>
        <option value="SHALL">SHALL</option>
      </select>
      <span>{{ errors.first(`${label}.type`) }}</span>
    </div>
    <div>
      <label :for="label + '.description'">Decsription:</label>
      <input
        :name="label + '.description'"
        v-model="description"
        v-validate.disable="'required|min:5|max:10'"
      />
      <span>{{ errors.first(`${label}.description`) }}</span>
    </div>
  </div>
</template>

<script>
export default {
  inject: {
    $validator: "$validator"
  },
  props: {
    label: String
  },
  data() {
    return {
      type: null,
      description: null
    };
  }
};
</script>
