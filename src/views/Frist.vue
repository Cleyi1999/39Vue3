<template>
    <div>
        <h1>问卷调查表填写</h1><br>
        <p>1.请问您的性别是：</p>
        <p><input type="radio" name="sex"  value="男" v-model="sex">男
            <input type="radio" name="sex" value="女" v-model="sex">女
            <input type="radio" name="sex" >保密</p>
        <button @click="Sex()">下一页</button>
    </div>
</template>

<script>

    export default {
        name: "Frist",
        data(){
            return{
                sex:''
            }
        },
        methods:{
            Sex(){
                this.$router.push('/Second')
                this.$store.commit("doSex",this.sex)
            },
        }
    }
</script>

