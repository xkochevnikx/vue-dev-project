<template>
    <div class="app">
        <form action="">
            <input
                class="input"
                type="text"
                placeholder="название" />
            <input
                class="input"
                type="text"
                placeholder="описание" />
            <button class="btn">Cоздать</button>
        </form>
        <div
            class="post"
            v-for="post in posts">
            <div>{{ post.title }}</div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            posts: [
                { id: 1, title: 'JavaScript', body: 'Лучший язык на свете' },
                { id: 1, title: 'JavaScript2', body: 'Лучший язык на свете' },
                { id: 1, title: 'JavaScript3', body: 'Лучший язык на свете' },
            ],
        };
    },
    methods: {
        addLike() {
            this.likes += 1;
        },
        disLike() {
            this.likes -= 1;
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

.post {
    padding: 20px;
    border: solid 2px orange;
    margin: 5px;
}

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
