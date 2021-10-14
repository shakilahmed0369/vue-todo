<template>
    <div class="row flex">
        <input
            v-model="addTask.task"
            type="text"
            class="p-2 w-full border-green-400 rounded-l border-l-4 focus:outline-none"
        />
        <input
            @click="handleInput"
            type="button"
            value="Add"
            class="p-2 bg-green-400 rounded-r text-white cursor-pointer hover:bg-green-500"
        />
    </div>
</template>
<script>
export default {
    data() {
        return {
            addTask:
            {
                task: '',
                done: false
            }
        }
    },
    created() {

    },
    methods: {
        handleInput() {
            // alert(this.addTask.task);
            this.$emit('addTask', this.addTask)
            this.addTask.task = ''
        }
    },

}
</script>
<style lang="">
    
</style>