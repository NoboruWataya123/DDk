<script></script>

<section class="container">
    <div class="main">
        <img class="main_img" src="/desert.webp" alt="desert" />
    </div>
    <div class="secondary">
        <article class="secondary__article">
            <img class="secondary__article_img" src="/sea.webp" alt="sea" />
        </article>
        <article class="secondary__article">
            <img
                class="secondary__article_img"
                src="/jungle.webp"
                alt="jungle"
            />
        </article>
    </div>
</section>

<style>
    .container {
        width: 100%;
        height: 70%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
    }
    .main {
        margin: 1rem;
        width: 60%;
        height: 100%;
    }
    .secondary {
        display: flex;
        flex-direction: column;
        align-items: space-between;
        justify-content: space-between;
        width: 40%;
        height: 100%;
        margin: 1rem;
    }
    .secondary__article {
        width: 100%;
        height: 47%;
    }
    .main_img {
        width: 100%;
        height: 100%;
    }
    .secondary__article_img {
        width: 100%;
        height: 100%;
    }
</style>
