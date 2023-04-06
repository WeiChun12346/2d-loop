<template>
  <div id="app">
    <div
      style="border: 1px solid lightgrey; margin: 20px; padding: 50px"
      v-for="(x, idx) in logs1"
    >
      <div v-for="(j, i) in x">
        {{ j.title }}
        <div v-for="(k, i) in j.data">{{ k.field }} {{ k.value }}</div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data() {
    return {
      logs1: [
        [
          {
            title: 'CREATED_DRAFT_APPLICATION',
            created_by_name: 'Li',
            action: '',
            description: '',
            data: [
              {
                field: '',
                value: 'If Owner Respone = Accepted',
              },
              {
                field: 'STATUS',
                value: 'DELETED',
              },
            ],
          },
          {
            title: 'DELETED_DRAFT_APPLICATION',
            created_by_name: 'Li',
            action: '',
            description: '',
            data: [
              {
                field: 'STATUS',
                value: 'DELETED',
              },
            ],
          },
        ],
        [
          {
            title: 'CREATED_DRAFT_APPLICATION',
            created_by_name: 'Li',
            action: '',
            description: '',
            data: [],
          },
        ],
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
