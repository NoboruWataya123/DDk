<script lang="ts">
    let name = "SvelteKit";
    import Navbar from "../components/Navbar.svelte";
</script>

<div class="container">
    <div class="header__line" />
    <div class="main">
        <Navbar />
        <slot />
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
        height: 2%;
        background-color: #000;
    }
    .main {
        width: 100%;
        height: 90%;
        padding: 0 5% 0 5%;
    }
    @media screen and (max-width: 600px) {
        .container {
            width: 100%;
            min-height: 100vh;
        }
        .main {
            width: 100%;
        }
    }
</style>
