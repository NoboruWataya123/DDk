<script></script>

<section class="container">
    <nav class="nav">
        <div class="nav__logo">
            <!-- <img
                class="nav__logo_img"
                src="https://unsplash.it/200/200?image=10"
                alt="SvelteKit"
            /> -->
            <a href="/">Placeholder</a>
        </div>
        <div class="nav__menu">
            <a href="https://sveltekit.com/docs">Docs</a>
            <a href="https://sveltekit.com/blog">Blog</a>
            <a href="https://sveltekit.com/community">Community</a>
            <a href="https://sveltekit.com/contribute">Contribute</a>
        </div>
        <div>
            <a class="login" href="login">Login</a>
        </div>
    </nav>
</section>

<style>
    .container {
        width: 100%;
        height: 15%;
    }
    .nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        height: 100%;
        flex-direction: row;
    }
    .nav__logo a {
        font-size: 1.5rem;
        font-style: italic;
        font-weight: bold;
        margin: 0 0 0 1rem;
    }
    .nav__menu {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        width: 40%;
        height: 100%;
    }
    a {
        text-decoration: none;
        color: #000;
        font-size: 1.2rem;
    }
    .login {
        background-color: #000;
        width: 100%;
        color: #fff;
        border: none;
        border-radius: 5px;
        padding: 0.5rem 1rem;
        font-size: 1.2rem;
        cursor: pointer;
        margin: 0 1rem 0 0;
    }
    .login:focus {
        outline: none;
    }
    .login:hover {
        background-color: rgb(78, 68, 68);
        color: rgb(255, 255, 255);
    }
    /* scale on click */
    .login:active {
        transform: scale(0.95);
    }
</style>
