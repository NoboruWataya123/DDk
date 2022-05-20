<script>
    export let id = "";
    export let imgsrc = "";
    export let title = "";
    export let content = "";
</script>

<article class="secondary__article">
    <div class="secondary__article_block">
        <a href={`/articles-${id}`}>
            <img class="secondary__article_img" src={imgsrc} alt="sea" />
        </a>
    </div>
    <div class="secondary__article_block">
        <a class="secondary__article_heading" href={`/articles-${id}`}
            >{title}</a
        >
        {content}
    </div>
</article>

<style>
    .secondary__article {
        width: 100%;
        display: flex;
        flex-direction: row;
        height: 47%;
    }
    .secondary__article_block {
        width: 50%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        text-align: center;
    }
    /* every odd element is 70% witdh */
    .secondary__article_block:nth-child(odd) {
        width: 50%;
    }
    .secondary__article_img {
        width: 100%;
        height: 100%;
    }
    .secondary__article_heading {
        font-size: 1.5rem;
        font-weight: bold;
        color: #000;
        text-decoration: none;
    }
</style>
