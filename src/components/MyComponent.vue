<template>
    <div>
        {{msg}}
        <video id="videoElement"></video>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import flvjs from 'flv.js'

@Component({
    data(){
        return {
            msg:"@Component"
        }
    },
    methods:{
        
    }
})


export default class MyComponent extends Vue{
    mounted (){
        this.loadPlayer();
    }

    loadPlayer(){
        if (flvjs.isSupported()) {
            let videoElement:any = document.getElementById('videoElement');
            let flvPlayer = flvjs.createPlayer({
                type: 'flv',
                url: 'http://127.0.0.1/flv/7182741.json'
            });
            flvPlayer.attachMediaElement(videoElement);
            flvPlayer.load();
            flvPlayer.play();
        }
    }
}
</script>

<style scoped lang="less">

</style>