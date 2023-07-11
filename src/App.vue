<template>
  <Layout>
    <form class="form-task">
      <input type="text" class="form-task__input" placeholder="Add new task" />
      <button class="form-task__button">Create Task</button>
    </form>

    <div class="no-result">
      <span>🙄</span>
      <br />
      <strong>No Items yet...</strong>
    </div>

    <template>
      <div class="task-container">
        <div class="card-task">
          <input type="checkbox" class="card-task__checkbox" />

          <strong class="card-task__name"></strong>
          <button type="button" class="card-task__button">❌</button>
        </div>
      </div>
    </template>

    <div class="loading-container">
      <strong>Loading...</strong>
    </div>
  </Layout>
</template>

<script lang="ts">
import Layout from './layouts/default.vue';

import { defineComponent } from 'vue';

export default defineComponent({
  components: { Layout },
});
</script>

<style lang="scss">
  $primary-color: #3498db;
  $white-color: #ffffff;
  $gray-color: #f1f1f1;
  $border: 10px;
  $padding: 10px;

  .form-task {
    width: 100%;
    display: flex;

    &__input {
      all: initial;
      width: calc(65% - 1rem);
      background-color: $gray-color;
      padding: $padding;
      border-radius: $border;
    }
  }
</style>
