<script>
    import { writable } from 'svelte/store';

    // Create a writable store for count
    export const count = writable(0);

    function increment() {
        count.update(n => n + 1);
    }
</script>

<div>
    <h2>Button</h2>
    <button on:click={increment}>Increment</button>
</div>
