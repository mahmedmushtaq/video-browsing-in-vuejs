<template>
    <li class="list-group-item media d-flex flex-wrap" @click="clickVideo">
<!--        <img class="mr-3" :src="thumbnailUrl">-->
        <div class="media-body">
            {{video.title}}
        </div>
    </li>
</template>

<script>
    export default{
        name:'VideoListItem',
        props:['video'],
        computed:{

        },
        methods:{
            clickVideo(){
                console.log("this video is = ",this.video);
                return this.$emit("onClick",this.video);
            }
        }
    }
</script>
