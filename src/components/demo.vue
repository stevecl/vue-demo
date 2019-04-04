<template>
    <div class="wrap">
        <div class="content text-gradient">
            <span>{{test}}</span>
        </div>
        <div class="content">
            <span class="text-gradient">{{test}}</span>
        </div>
        <div class="content">
            <span>{{test}}</span>
        </div>
        <button @click="clickHandle">click</button>
    </div>
</template>
<script>
export default {
    data(){
        return {
            test: 0
        }
    },
    methods: {
        clickHandle(){
            this.test = (Math.random() * 1000).toFixed(2);
        }
    }
}
</script>
<style lang="less" scoped>
.text-gradient {
  background: linear-gradient(to top, #8147FC, #D9B6FF);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.content{
    display: flex;
    width: 600px;
    height: 50px;
    line-height: 50px;
    margin: 0 auto 20px;
    border-bottom: 1px solid #888;
    span{
        flex: 1;
    }
}
</style>


