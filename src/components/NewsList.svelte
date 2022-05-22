<script>
    let articles = [
        {
            id: "1",
            title: "Keyboard Cat",
            imgsrc: "/sea.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-01-01",
        },
        {
            id: "2",
            title: "Maru",
            imgsrc: "/jungle.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-01-01",
        },
        {
            id: "3",
            title: "Henri The Existential Cat",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-01-01",
        },
        {
            id: "4",
            title: "Henri 2",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-01-31",
        },
        {
            id: "5",
            title: "Henri 3",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-01-22",
        },
        {
            id: "6",
            title: "Henri 3",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-12-01",
        },
        {
            id: "7",
            title: "Henri 4",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-05-01",
        },
        {
            id: "8",
            title: "Henri 5",
            imgsrc: "/desert.webp",
            content:
                "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Excepturi, alias!",
            date: "2020-10-01",
        },
    ];
</script>

<section class="container">
    <!-- table with articles -->
    <table class="main">
        {#each articles as { id, title, content, date }, i}
            <a class="main_links" href={`/articles-${id}`}>
                <tr class="main__block">
                    <td class="main__block_article">{title} <br /> {content}</td
                    >
                    <span class="main__block_date">{date}</span>
                </tr>
            </a>
        {/each}
    </table>
</section>

<style>
    .container {
        margin: 3rem 1rem 2rem 1rem;
        padding: 0 1rem 0 0;
        width: 60%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: row;
    }
    .main {
        width: 100%;
        height: 100%;
    }
    .main_links {
        text-decoration: none;
        color: black;
    }
    .main__block {
        width: 100%;
        border-radius: 0px;
        background: linear-gradient(315deg, #ffffff, #e6e6e6);
        box-shadow: -11px -11px 22px #dedede, 11px 11px 22px #ffffff;
        margin: 1rem 0;
        display: flex;
        flex-direction: row;
        /* center by y axis */
        align-items: center;
    }
    .main__block_article {
        width: 85%;
        height: 100%;
        align-self: center;
        padding: 1rem;
    }
    .main__block_date {
        width: 15%;
    }

    @media screen and (max-width: 600px) {
        .container {
            width: 100%;
        }
        .main {
            width: 100%;
        }
        .main__block {
            width: 100%;
            height: 100%;
        }
        .main_links {
            width: 100vw;
        }
        .main__block_article {
            width: 4rem;
            width: 60vw;
            text-overflow: ellipsis;
            overflow: hidden;
            white-space: nowrap;
        }
    }
</style>
