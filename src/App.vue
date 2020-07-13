<template>
    <div>
       <SearchBar @termChange="onTermChange"/>
        <VideoList :videos="videos"/>

    </div>
</template>


<script>
    import SearchBar from "./components/SearchBar";
    import VideoList from "./components/VideoList";
    const youtubeAPIKEY = 'AIzaSyB7ydlY1Gd8TUzZdZ-Mev9HPt8fwDxBg7U';
    import axios from "axios";
    export default {
        name:'App',
        components:{
            SearchBar,
            VideoList
        },
        data(){
           return{
               videos:[],
           }
        },
        methods:{
            async onTermChange(searchValue){
            const response = await  axios.get('https://www.googleapis.com/youtube/v3/search',{
                 params:{
                     key:youtubeAPIKEY,
                     type:'video',
                     part:'snippet',
                     q:searchValue,
                 }
             })


                this.videos = response.data.items;


            }
        }
    }
</script>
