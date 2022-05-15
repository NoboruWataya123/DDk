<script lang="ts">
    let name = "SvelteKit";
    import Navbar from "../components/Navbar.svelte";
</script>

<div class="container">
    <div class="header__line" />
    <div class="main">
        <Navbar />
    </div>
</div>

<style>
    .container {
        align-items: center;
        justify-content: center;
        height: 100vh;
    }
    .header__line {
        width: 100%;
        height: 5%;
        background-color: #000;
    }
    .main {
        width: 100%;
        height: 90%;
        display: flex;
        padding: 0 5% 0 5%;
    }
</style>
