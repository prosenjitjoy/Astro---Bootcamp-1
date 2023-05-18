<script lang="ts">
    export let messages: string[];
    const randomMessage = () => {
        const randomIndex = Math.floor(Math.random() * messages.length);
        greeting = messages[randomIndex];
    };
    $: greeting = messages[0];
</script>

<div>
    <h3>{greeting}! Thank you for visiting</h3>
    <button on:click={randomMessage}>New Greeting</button>
</div>

<style>
    button {
        padding: 0.5rem 1rem;
        color: white;
        background-color: #4c1d95;
        text-decoration: none;
    }
</style>
