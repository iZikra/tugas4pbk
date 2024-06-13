<template>
  <div id="app">
    <ParentComponent ref="parentComponent">
      <ChildComponent1 @send-message="receiveMessageFromChild" />
      <ChildComponent2 @send-message="receiveMessageFromChild" />
      <ChildComponent3 @send-message="receiveMessageFromChild" />
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';
import ChildComponent1 from './components/ChildComponent1.vue';
import ChildComponent2 from './components/ChildComponent2.vue';
import ChildComponent3 from './components/ChildComponent3.vue';

export default {
  name: 'App',
  components: {
    ParentComponent,
    ChildComponent1,
    ChildComponent2,
    ChildComponent3
  },
  methods: {
    receiveMessageFromChild(message) {
      this.$refs.parentComponent.receiveMessage(message);
    }
  }
};
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
