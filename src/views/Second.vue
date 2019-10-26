<template xmlns="http://www.w3.org/1999/html">
    <div>
        <h1>问卷调查表填写 </h1>
        <p>2.请选择兴趣爱好</p>
        <label><input type="checkbox" name="like" v-model="like" value="看书" >看书</label>
        <label><input type="checkbox" name="like" v-model="like" value="游泳">游泳</label>
        <label><input type="checkbox" name="like" v-model="like" value="跑步">跑步</label>
        <label><input type="checkbox" name="like" v-model="like" value="电影">电影</label>
        <label><input type="checkbox" name="like" v-model="like" value="音乐">音乐</label>
        <label><input type="checkbox" name="like" v-model="like" value="动漫">动漫</label><br>
        <button><router-link to="/">上一步</router-link></button>
        <button @click="doChoice()">下一步</button>
        <button @click="doQt()">全选</button>
    </div>
</template>

<script>
    export default {
        name: "Second",
        data(){
            return{
               like:[]
            }
        },
        methods:{
            doChoice(){
                this.$router.push("/Third")
                this.$store("doChoice",this.like)
            },
            doQt(){
                this.like='""'
            }
        }
    }
</script>

<style scoped>
button{text-decoration: none;margin-left: 50px}
</style>