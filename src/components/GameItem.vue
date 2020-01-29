<template>
    <div class="todo-item" v-bind:class="{'is-complete':game.completed}">
        <div class="container">

            <button @click="$emit('del-game', game.id)" class="del">x</button>
            <div class="clear"></div>

            <h2><label><input type="checkbox" v-on:change="markComplete">{{game.title}}</label></h2>

            <div class="content-container" v-bind:class="{'is-complete':game.completed}">

            <div class="des left">
            <p>{{game.description}}</p>
            </div>

                <div class="img right">
                <img v-bind:src="game.image">
                </div>

                <div class="clear"></div>

            </div>

        </div>
    </div>
</template>

<script>
    export default {
        name: "GameItem",
        props: ["game"],
        methods: {
            markComplete(){
                this.game.completed = !this.game.completed;
            }
        }
    }
</script>

<style scope>

    .todo-item {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 1px #ccc dotted;
    }
    .is-complete {
        text-decoration: line-through;
        opacity: .5;
        transition: opacity ease 1s;
    }
    .del {
        background: #ff0000;
        color: #fff;
        border: none;
        padding: 5px 9px;
        border-radius: 10px;
        cursor: pointer;
        float: right;
        margin: 10px;
    }
    .left{
        float: left;
    }
    .right{
        float: right;
    }
    .clear{
        clear: left;
        clear: right;
    }
    .des{
        width: 50%;
        text-align: justify;
        margin-left: 1em;
    }
    .img{

    }
    img{
        border-radius: 10px;
        margin-bottom: 1.8em;
        margin-right: 2em;

    }
    .container{
        border: solid 1px #333333;
        border-radius: 10px;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.1), 0 6px 20px 0 rgba(0, 0, 0, 0.01);
        background-color: white;
        max-width: 80em;
        margin: 0 auto;
    }
    input{
        visibility: hidden;
    }
</style>