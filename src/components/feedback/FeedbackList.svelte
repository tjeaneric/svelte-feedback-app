<script>
    import { feedbackStore } from '../../stores/stores';
    import {fade, scale } from 'svelte/transition'
    import FeedbackItem from "./FeedbackItem.svelte";

 
</script>

{#each $feedbackStore as fb (fb.id) }
<div in:scale out:fade={{duration:500}}>
    <FeedbackItem item={fb} />
</div>
{/each}
    