<template>
    <div id="list">
        <div class="tasks" v-for="(task, index) in tasks" :key="index" :style="task.cor" >
            {{task.text}}
        </div>
        
    </div>
</template>

<script>
export default {
    name: "list",
    props: ['tasks']
}
</script>

<style>
    #list{
        color: #FFF;
        display: flex;
        width: 700px;
        height: 200px;
        border: 1px solid #FFF;
        margin: 200px auto 0 auto;
        flex-wrap: wrap;
    }
    .tasks{
        width: 150px;
        height: 30px;
        border: 1px solid #FFF;   
        margin: 10px 0 0 10px;
        text-align: center;
        line-height: 30px;
        user-select: none;
        cursor: pointer;
    }
</style>