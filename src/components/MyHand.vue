<template>
     <div class="hand">
        <div class="handcard" v-for="(card,index) in cards" :style="cardPos(index)" :key="index">
            {{ card.name }}
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            cards:[]
        }
    },
    mounted(){
        for(let i=0;i<5;i++)
        this.cards.push({
            name: "some card",
            desc: "this card is awesome"
        })
    },
    methods:{
        cardPos(pos){
            console.log("position:"+pos);
        }
    }
}
</script>

