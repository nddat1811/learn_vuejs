<template>
  <div class="demo-ref">
    <h1>Demo ref</h1>
    <button class="avatar"
        v-on:click="handleClickInputFile">
        Thay đổi avatar
    </button>
    <input type="file"
        style="display:none"
        ref="fileInputAvatar">
  </div>
</template>

<script>
export default {
    name: 'demo-ref',
    data(){
        return {

        }
    },
    methods: {
        handleClickInputFile(e) {
            this.$refs.fileInputAvatar.click()
        }
    }
}
</script>

<style>
    .demo-ref {
        margin-top: 100px;
        padding: 100px 30px;
        border: 1px solid #000;
    }
    .avatar {
        color:#fff;
        border: 2px solid #333;
        padding: 12px 15px;
        background-color: #333;
    }
    .avatar:hover{
        color: #333;
        background-color: #fff;
    }
</style>