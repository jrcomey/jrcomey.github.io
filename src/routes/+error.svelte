<script>
    import { page } from '$app/stores';
    import Header from './Header.svelte';
</script>

<Header/>


<section class="error">
    <h1>{$page.status}: {$page.error.message}</h1>

    <a href="/">
        <h2>Go to homepage</h2>
    </a>
</section>




<style>

.error {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    align-items: center;
}
    
</style>