<template>
  <div>
    <!-- v-if and v-else -->
    <div>
      <h2>v-if and v-else:</h2>
      <p v-if="showMessage">This message is shown using v-if.</p>
      <p v-else>This message is shown using v-else.</p>
    </div>

    <!-- v-show -->
    <div>
      <h2>v-show:</h2>
      <p v-show="showMessage">This message is shown using v-show.</p>
    </div>

    <!-- v-for -->
    <div>
      <h2>v-for:</h2>
      <ul>
        <li v-for="(item, index) in items" :key="index">{{ item }}</li>
      </ul>
    </div>

    <!-- v-if with v-for -->
    <div>
      <h2>v-if with v-for:</h2>
      <div v-for="(item, index) in itemsWithConditions" :key="index">
        <p v-if="item.show">{{ item.text }}</p>
      </div>
    </div>

    <!-- Form Input Handling -->
    <div>
      <h2>Form Input Handling:</h2>
      <label for="inputText">Input Text:</label>
      <input type="text" id="inputText" v-model="inputValue">
      <p>Input Value: {{ inputValue }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMessage: true,
      items: ['Item 1', 'Item 2', 'Item 3'],
      inputValue: '',
      itemsWithConditions: [
        { text: 'Item A', show: true },
        { text: 'Item B', show: false },
        { text: 'Item C', show: true },
      ],
    };
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>
