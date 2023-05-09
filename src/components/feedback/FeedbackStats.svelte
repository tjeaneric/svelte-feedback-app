<script>
    import { feedbackStore } from "../../stores/stores";

   $: count = $feedbackStore.length
   $: average = $feedbackStore.reduce((a, {rating})=> a+rating, 0)/$feedbackStore.length
</script>

<div class="feedback-stats">
    <h4>{count} Review{count ==1? '':'s'}</h4>
    <h4>Ratings Average: {average? average: 0}</h4>
</div>

<style>
    .feedback-stats{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>