<template>
    <div>
        <ul class="list-group">
            <VideoListItem
                    v-for="(video,index) in videos"
                    :video="video" :key="index"
                    @onClick="videoOnClick"
            >

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
        methods:{
            videoOnClick(video){
                console.log('video is = ',video);
            }
        }


    }
</script>
