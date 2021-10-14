<template lang="">
  <div>
    <p v-if="tasks.length < 1" class="text-center">
      <img class="object-position: center inline" src="https://c.tenor.com/20lggg8cjOMAAAAM/rage-anime.gif" alt="" />
      <div class="font-bold">Do some work you piece of shit</div>
    </p>
    <div v-for="(task, index) in tasks" :key="index">
      <li
        :key="task.taks"
        v-if="task.done == true"
        class="text-lg text-red-400 py-1"
      >
        <span class="cursor-pointer" @click="handleTask(index)">[ x ] </span>
        <del>{{ task.task }}</del>
        <span
          class="
            text-red-500
            float-right
            cursor-pointer
            hover:text-red-800
            font-bold
          "
          @click="handleDeleteTask(index)"
          >x</span
        >
      </li>
      <li v-else :key="task.task" class="text-lg text-green-400 py-1">
        <span class="cursor-pointer" @click="handleTask(index)">[ o ]</span>
        {{ task.task }}
        <span
          class="
            text-red-500
            float-right
            cursor-pointer
            hover:text-red-800
            font-bold
          "
          @click="handleDeleteTask(index)"
          >x</span
        >
      </li>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    tasks: Array,
  },
  methods: {
    handleTask(arrIndex) {
      this.tasks.filter((value, index) => {
        if (index == arrIndex) {
          value.done = !value.done;
        }
      });
    },

    handleDeleteTask(arrIndex) {
      this.tasks.splice(arrIndex, 1);
    },
  },
};
</script>
<style lang=""></style>
