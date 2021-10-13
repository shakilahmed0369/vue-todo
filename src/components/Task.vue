<template lang="">
    <div>
        <div v-for="(task, index) in tasks" :key="index">
            <li :key="task.taks" v-if="task.done == true" class="text-lg text-red-400 py-1"><span class=" cursor-pointer">[ x ]</span> <del>{{task.task}}</del>
                <span class="text-red-500 float-right cursor-pointer hover:text-red-800 font-bold">x</span>
            </li>
            <li  v-else :key="task.task" class="text-lg text-green-400 py-1 "><span class="cursor-pointer">[ o ]</span> {{task.task}}
                <span class="text-red-500 float-right cursor-pointer hover:text-red-800 font-bold">x</span>
            </li>
        </div>
        
    </div>
</template>
<script>
export default {
    props: {
        tasks:Array,
        
    },
}
</script>
<style lang="">
    
</style>