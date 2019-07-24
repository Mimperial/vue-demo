<template>
    <div>
        <button  @click="handleClick">{{content}}</button>
    </div>
</template>

<script>
    // 判断参数是否是其中之一
    function oneOf (value, validList) {
        for (let i = 0; i < validList.length; i++) {
            if (value === validList[i]) {
                return true;
            }
        }
        return false;
    }

    export default {
        name: "MButtom",
        props:{
            content: {
                validator (value) {
                    return oneOf(value, ['1', '2', '3']);
                },
                type:String,
                default:"我是默认的内容"
            }
        },
        methods:{
            handleClick(event){
                // eslint-disable-next-line no-console
                console.log(event.toString())
                var content = {name:"zilong",age:33};
                this.$emit('on-click', content);
            }
        }

    }
</script>

<style scoped>

</style>