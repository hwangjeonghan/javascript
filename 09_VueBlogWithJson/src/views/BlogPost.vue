<script setup>
import { useRoute } from "vue-router";
import { useBlogStore } from '../stores/blog';
import { watchEffect, ref } from "vue";

const { postBlog, postHandler } = useBlogStore();

const handler = () => {
    postHandler(postBlog);
}
</script>

<template>
    <div class="blogContainer">
        <div class="titleContainer">
            <input v-model="postBlog.title" placeholder="디지몬 도감을 보고 입력" class="" />
        </div>
        <div class="content">
            <div>
                <textarea v-model="postBlog.content"></textarea>
            </div>
            <div class="imgContainer">
                <div>
                    <label> 이미지 url 등록하기! </label>
                    <input class="imgInput" v-model="postBlog.img" />
                </div>
                <template v-if="postBlog.img">
                    <img class="imgBox" :src="postBlog.img" />
                </template>
            </div>
        </div>
        <button @click="handler">등록하기 </button>
    </div>
</template>

<style scoped>
.blogContainer {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70%;
    height: 700px;
    border: 1px solid;
    margin-left: auto;
    margin-right: auto;
    border-radius: 5%;
    background-color: white;

}

.titleContainer {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    margin-top: 5%;
    margin-bottom: 2%;
    margin-left: auto;
    margin-right: auto;

    
}

.title {
    width: 40%;

    text-align: center;
    border-bottom: 1px solid;
    
}

.contentContainer {
    text-align: center;
    width: 70%;
}

.content {

    text-align: left;
    margin-bottom: 2%;
    border: 1px;
    margin-top: 5%;
}

textarea {
    width: 100%;
    height: 200px;
}

.imgInput {
    width: 65%;
}

.imgBox {
    width: 300px;
    height: 300px;
}

.imgContainer {
    display: flex;
    flex-direction: column;
    margin-top: 15%;
    margin-left: 20%
}
</style>