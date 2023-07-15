<template>
    <div class="app">
        <post-form />
        <post-list :posts="posts" />
    </div>
</template>
<script>
import PostForm from './components/PostForm.vue';
import PostList from './components/PostList.vue';

export default {
    components: { PostForm, PostList },
    data() {
        return {
            posts: [
                { id: 1, title: 'JavaScript', body: 'Лучший язык на свете' },
                { id: 1, title: 'JavaScript2', body: 'Лучший язык на свете' },
                { id: 1, title: 'JavaScript3', body: 'Лучший язык на свете' },
            ],
            title: '',
            body: '',
        };
    },

    methods: {
        createPost() {
            const date = {
                id: Date.now(),
                title: this.title,
                body: this.body,
            };
            this.posts.push(date);
            this.title = '';
            this.body = '';
        },
    },
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: JetBrains Mono;
}

.app {
    padding: 20px;
}
</style>
