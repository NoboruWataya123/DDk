<script>
    import Article from "./Article.svelte";
    let articles = [
        {
            id: "1",
            title: "Keyboard Cat",
            imgsrc: "/sea.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
        },
        {
            id: "2",
            title: "Maru",
            imgsrc: "/jungle.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
        },
        { id: "3", title: "Henri The Existential Cat", content: "content123" },
    ];
</script>

<section class="container">
    <div class="main">
        <img class="main_img" src="/desert.webp" alt="desert" />
    </div>
    <div class="secondary">
        {#each articles as { id, title, imgsrc, content }, i}
            {#if i < 2}
                <Article {id} {imgsrc} {title} {content} />
            {/if}
        {/each}
    </div>
</section>

<style>
    .container {
        margin: 3rem 0 2rem 0;
        width: 100%;
        height: 55%;
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
        margin: 1rem 0 1rem 1rem;
    }
    .main_img {
        width: 100%;
        height: 100%;
    }
</style>
