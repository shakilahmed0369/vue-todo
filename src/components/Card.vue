<template>
    <div class="container mx-auto px-4">
        <div class="p-4 bg-gray-100 border border-green-400 rounded-lg">
            <Input @addTask="addTask" />
            <div class="py-4">
                <ul>
                    <Task :tasks="tasks" />
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
import Input from "./Input.vue";
import Task from "./Task.vue";
export default {

    components: {
        Input,
        Task,
    },

    data(){
        return {
            tasks: []
        }
    },
    methods: {
        addTask(event){
           this.tasks.push({task: event.task, done:event.done})
        },

        handleTask() {
            
        }
    }

}
</script>
<style >
    
</style>