<template>
    <div>
        <ul>
            <VideoListItem
                    v-for="(video,index) in videos"
                    :video="video" :key="index">

            </VideoListItem>
        </ul>
    </div>
</template>

<script>
    import VideoListItem from "./VideoListItem";
    export default {
        name:'VideoList',
        components:{
            VideoListItem,
        },
        props:['videos'],


    }
</script>
