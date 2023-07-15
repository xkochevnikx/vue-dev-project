<template lang="">
    <form
        action=""
        @submit.prevent>
        <input
            @input="post.title = $event.target.value"
            v-bind:value="post.title"
            class="input"
            type="text"
            placeholder="название" />
        <input
            @input="post.body = $event.target.value"
            v-bind:value="body"
            class="input"
            type="text"
            placeholder="описание" />
        <button class="btn">Cоздать</button>
    </form>
</template>
<script>
export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            },
        };
    },
};
</script>
<style scoped>
.input {
    width: 100%;
    border: 1px rgb(124, 124, 206) solid;
    padding: 10px 15px;
    margin: 5px;
}

.btn {
    background: none;
    padding: 5px 10px;
    margin: 5px;
    border-radius: 3px;
    width: 100%;
}
</style>
