<script lang="ts">
    import NewsList from "../components/NewsList.svelte";

    import FrontPage from "../components/FrontPage.svelte";

    let name = "SvelteKit";
</script>

<span class="container">
    <FrontPage />
    <NewsList />
</span>

<style>
    @media screen and (max-width: 600px) {
        .container {
            display: flex;
            flex-direction: column;
            z-index: 0;
        }
    }
</style>
