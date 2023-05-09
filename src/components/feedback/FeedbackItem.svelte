<script>
    import { feedbackStore } from "../../stores/stores";
    import BaseCard from "../ui/BaseCard.svelte";


    export let item
    const handleDelete = (itemId)=>{
        feedbackStore.update((currFb)=>currFb.filter(item => item.id != itemId))
    }
</script>

<BaseCard >
    <div class="num-display">
        {item.rating}
    </div>

    <button class="close" on:click={()=>handleDelete(item.id)}>X</button>
    <p class='text-display'>{item.text}</p>
</BaseCard>

<style>
    .num-display{
        position: absolute;
        padding:10px;
        text-align: center;
        font-size: 19px;
        top: -10px;
        left: -10px;
        width: 50px;
        height: 50px;
        background:#ff6a95;
        color:#fff;
        border: 1px #eee solid;
        border-radius: 50%;

    }
    .close{
        position: absolute;
        top:10px;
        right:20px;
        cursor: pointer;
        background: none;
        border: none;

    }
</style>