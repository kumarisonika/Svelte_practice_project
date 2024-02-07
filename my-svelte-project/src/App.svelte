<!-- App.svelte -->
<script>
    import ChildComponent from './ChildComponent.svelte';
    let parentData = 'Data from parent component';

    function handleChildEvent(event) {
        console.log('Event received from child component:', event.detail);
    }
</script>

<main>
    <h1>Dive deeper into Svelte components</h1>
    <p>{parentData}</p>
    <ChildComponent on:childEvent={handleChildEvent} />
</main>
