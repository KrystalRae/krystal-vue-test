<template>
    <v-card class="pa-3">
        <div>
            <span class="post-title">{{post.title}}</span>
        </div>
        <div>
            <span class="post-text">{{post.text}}</span>
        </div>
    </v-card>
</template>

<script>
export default {
    name: 'Post',
    props: {
        post: Object,
    }
}
</script>

<style>
.post-title{
    font-size: 16px;
    font-weight:bold;
}

.post-text{
    text-indent: 20px;
    
}


</style>