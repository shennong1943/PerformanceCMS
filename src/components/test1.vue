<template>
    <div>
        <el-button type="primary" @click.prevent="handleClick">
            热爱生命<i class="el-icon-arrow-down el-icon--right"></i>
        </el-button>
        <div class="box">
            <ul :style="{ maxHeight: isShow ? '255px' : '0px' }">
                <li>我不去想是否能够成功</li>
                <li>既然选择了远方</li>
                <li>便只顾风雨兼程</li>
                <li>我不去想能否赢得爱情</li>
                <li>既然钟情于玫瑰</li>
                <li>就勇敢地吐露真诚</li>
            </ul>
            <ul :style="{ height: isShow ? '255px' : '0px' }">
                <li>我不去想是否能够成功</li>
                <li>既然选择了远方</li>
                <li>便只顾风雨兼程</li>
                <li>我不去想能否赢得爱情</li>
                <li>既然钟情于玫瑰</li>
                <li>就勇敢地吐露真诚</li>
            </ul>
        </div>
        <div>
            既然目标是地平线,留给世界的只能是背影
        </div>
    </div>
</template>
<script>
export default {
    name: 'CommonAnimation',
    data() {
        return {
            isShow: false,
        }
    },
    methods: {
        handleClick() {
            this.isShow = !this.isShow
        },
    },
};
</script>
<style lang='less' scoped>
.box {
    margin: auto;
    display: flex;
}
ul,
li {
    list-style: none;
    margin: 0;
    padding: 0;
}
ul {
    width: 200px;
    margin: auto;
    margin-top: 10px;
    // border: 0px solid transparent;
    border-radius: 5px;
    background-color: rgb(99, 175, 236);
    transition: height .3s, max-height .6s;
    overflow: hidden;
}
li {
    padding: 10px 0;
    border-bottom: 1px solid skyblue;
    &:last-child {
        border-bottom: none;
    }
}
</style>
