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
        {
            id: "3",
            title: "Henri The Existential Cat",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
        },
    ];
</script>

<section class="container">
    <div class="main">
        <a href={`/articles-${articles[0].id}`}
            ><img class="main_img" src={articles[0].imgsrc} alt="desert" />
        </a>
        <div class="main_block">
            <a class="main_heading" href={`/articles-${articles[0].id}`}
                >{articles[0].title}</a
            >
            {articles[0].content}
        </div>
    </div>
    <div class="secondary">
        {#each articles as { id, title, imgsrc, content }, i}
            <!-- scipr first element -->
            {#if i != 0 && i < 3}
                <Article {id} {imgsrc} {title} {content} />
            {/if}
        {/each}
    </div>
</section>

<style>
    .container {
        margin: 3rem 0 2rem 0;
        width: 100%;
        height: 60%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
        z-index: 0;
    }
    .main {
        margin: 0 1rem 0 1rem;
        width: 60%;
        height: 100%;
        position: relative;
    }
    .main_block {
        /* pop up overlay inside image who shows on bottom */
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 20%;
        background: rgba(0, 0, 0, 0.17);
        display: flex;
        align-items: flex-start;
        justify-content: center;
        flex-direction: column;
        padding: 0 0 0 2rem;
        color: hsl(0, 0%, 100%);
    }
    .main_block:hover {
        background: rgba(0, 0, 0, 0.5);
        transition: all 0.5s ease;
    }
    .main_heading {
        font-size: 1.5rem;
        font-weight: bold;
        color: #fff;
        text-decoration: none;
    }
    .secondary {
        display: flex;
        flex-direction: column;
        align-items: space-between;
        justify-content: space-between;
        width: 40%;
        height: 100%;
    }
    .main_img {
        width: 100%;
        height: 100%;
    }

    /* create media query for mobile design one column */
    @media screen and (max-width: 600px) {
        .container {
            flex-direction: column;
            width: 100%;
            height: 100%;
            margin: 5rem 0 2rem 0;
            z-index: 0;
        }
        .main {
            width: 100%;
            margin: 0 0 1rem 0;
        }
        .main_block {
            position: absolute;
            bottom: 10%;
            left: 0;
            width: 100%;
            height: 20%;
            padding: 0 1rem 0 2rem;
            font-size: 0.7rem;
            background: rgba(0, 0, 0, 0.5);
        }
        .main_img {
            width: 100%;
            height: 100%;
        }
        .secondary {
            width: 100%;
            min-height: 100%;
            flex-direction: column;
        }
    }
</style>
