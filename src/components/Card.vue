<template>
    <div class="container">
        <div class="p-4 bg-gray-100 border border-green-400 rounded-lg mx-4">
            <Input />
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
            tasks: [
                {
                    task: 'go for morning walk',
                    done: true,

                },
                {
                    task: 'go for morning walk',
                    done: false,

                },

            ]
        }
    },



}
</script>
<style >
    
</style>