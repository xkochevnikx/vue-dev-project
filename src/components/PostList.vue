<template lang="">
    <div
        class="post"
        v-for="post in posts">
        <div>{{ post.title }}</div>
    </div>
</template>
<script>
export default {
    props: {
        posts: {
            type: Array,
            required: true,
        },
    },
};
</script>
<style scoped>
.post {
    padding: 20px;
    border: solid 2px orange;
    margin: 5px;
}
</style>
