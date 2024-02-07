<!-- ChildComponent.svelte -->
<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    let childData = 'Data from child component';

    function sendDataToParent() {
        dispatch('childEvent', childData);
    }
</script>

<section>
    <h2>Child Component</h2>
    <p>{childData}</p>
    <button on:click={sendDataToParent}>Send Data to Parent</button>
</section>
