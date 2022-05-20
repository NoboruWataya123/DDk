<script lang="ts">
    import Article from "../components/Article.svelte";
    import { onMount } from "svelte";
    import { page } from "$app/stores";

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
    let res: any;

    let findArticleById = (id: any) => {
        return articles.find((article: any) => article.id === id);
    };
    onMount(async () => {
        res = findArticleById($page.params.id);
    });
</script>

<div class="container">
    <Article {...res} />
</div>

<style>
</style>
