<template>
    <div class="hello">
        <h1>{{title}}</h1>
        <p>{{message}}</p>
        <hr />
        <button v-on:click="doAction">Show/Hide</button>
        <transition name="transit">
            <p v-if="flg" class="trans">Transition!!!!</p>
        </transition>
    </div>
</template>

<script>
    export default {
        name: 'HelloWorld',  //Calcとしてexport
        props: {
            title: String,
        },
        data: function () {
            return {
                message: 'transition sampleですいういういういい',
                flg: true,
                btn: 'show/hide',
            };
        },
        methods:{
            doAction: function () {
                this.flg = !this.flg;
            },
        },
    }
</script>
<style>
div.out {
  padding: 5px 0px;
  background-color: #eee;
  width:300px;
  height:200px;
}
div.mid {
  padding: 5px 0px;
  background-color: #ddd;
  width:200px;
  height:175px;
}
div.in {
  padding: 5px 0px;
  background-color: #ccc;
  width:100px;
  height:150px;
}
.area{
    width: 300px;
    height: 100px;
    background-color: #ddd;
    padding: 10px;
    font-size: 20pt;
}
.inner {
    color: red;
    font-size: 14pt;
}
.etc {
    color: green;
    background-color: #eee;
    font-size: 12pt;
    padding: 5px;
}
.trans{
    width: 150px;
    background-color: #ddf;
    padding: 10px;
    font-size: 20pt;
}
.transit-enter-active{
    transition: 1.0s;
}
.transit-leave-active{
    transition: 1.0s;
}
.transit-enter, .transit-leave-to {
    transform: translateX(200px) translateY(-200px);
    opacity: 0.1;
}
.transit-enter, .transit-leave-to{
    transform: rotateZ(180deg);
    opacity: 0.1;
}
.transit-leave-active{
    animation: anim 5.0s;
}
.transit-enter-active{
    animation: anim 2.5s reverse;
}

@keyframes anim{
    0% {
        transform: translateX(0px) translateY(0px) rotateZ(0deg);
        opacity: 1.0;
        background-color: #ddf;
     }
     25% {
         transform: translateX(250px) translateY(0px) rotateZ(0deg);
        opacity: 1.0;
        background-color: #fdd;
     }
     50% {
        transform: translateX(0px) translateY(-100px) rotateZ(540deg);
        opacity: 1.0;
        background-color: #dfd;
     }
     75% {
        transform: translateX(250px) translateY(-100px) rotateZ(0deg);
        opacity: 1.0;
        background-color: #fdf;
     }
     100% {
        transform: translateX(0px) translateY(-200px) rotateZ(1080deg);
        opacity: 1.0;
        background-color: #ffd;
     }
}
</style>