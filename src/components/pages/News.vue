<script>
import NewsItem from "../widgets/NewsItem.vue";
import NewsItemFooter from "../widgets/NewsItemFooter.vue";
import TimeStamp from "../widgets/TimeStamp.vue";
export default {
    data() {
        return {
            featuredArticle: {
                imageUrl: "https://images.performgroup.com/di/library/omnisport/79/d8/6c9b4b26f64a40ea89b7f69ccd088d40.jpg?t=-955230179&w=640",
                title: "Inter boss Simone Inzaghi reveals admiration for Diego Simeone ahead of clash",
                gmtTime: "2024-02-19T20:04:27.000Z",
                source: "FotMob",
                lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                pageURL: "https://www.fotmob.com/news/138lzxhk8mmsi1nflku3xemdte-inter-boss-simone-inzaghi-reveals-admiration-diego-simeone-ahead-clash"
            },
            articles: [
                {
                    imageUrl: "https://images2.minutemediacdn.com/image/upload/c_crop,w_7033,h_3956,x_0,y_132/c_fill,w_1080,ar_16:9,f_auto,q_auto,g_auto/images%2FGettyImages%2Fmmsport%2F90min_en_international_web%2F01hqxbvkpj6py3em8f47.jpg",
                    title: "Chelsea keen to replace Marc Cucurella with £15m Englishman - report",
                    gmtTime: "2024-03-01T18:18:00.000Z",
                    source: "FotMob",
                    lead: "Chelsea are ready to sell left-back Marc Cucurella as they prepare for a summer overhaul of the position, a report has claimed.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/embed/news/01hqxb18wwzf/chelsea-keen-replace-marc-cucurella-15m-englishman"
                },
                {
                    imageUrl: "https://theanalyst.com/wp-content/uploads/2024/03/longest-scoring-streaks-premier-league.jpg",
                    title: "The Longest Premier League Scoring Streaks by Teams",
                    gmtTime: "2024-03-01T18:24:00.000Z",
                    source: "The Analyst",
                    lead: "With Tottenham having scored in every one of their league games since March 2023, we chart the teams to have found the net at least once in the most consecutive Premier League games.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://theanalyst.com/na/2024/03/longest-premier-league-scoring-streaks-teams/"
                },
                {
                    imageUrl: "https://images.performgroup.com/di/library/omnisport/32/42/bf6d140ca28448e28254473502bb9720.jpg?t=220078590&w=1200&h=630",
                    title: "Thomas Tuchel plays down suggestions Lazio loss could hasten his Bayern exit",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "Simone Inzaghi and Diego Simeone, now boss of Atletico Madrid, helped Lazio win Serie A as players in 2000.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/news/j90vt75vwsu917hnu7r6t7v44-thomas-tuchel-plays-down-suggestions-lazio-loss-could-hasten-his-bayern-exit"
                },
                {
                    imageUrl: "https://images2.minutemediacdn.com/image/upload/c_crop,w_6795,h_3822,x_2001,y_81/c_fill,w_2160,ar_16:9,f_auto,q_auto,g_auto/images%2FGettyImages%2Fmmsport%2F90min_en_international_web%2F01hr4g90hgxp7q5mp6jx.jpg",
                    title: "Rafael Leao gives definitive response to Chelsea & PSG transfer rumours",
                    gmtTime: "2024-02-19T20:04:27.000Z",
                    source: "FotMob",
                    lead: "AC Milan forward Rafael Leao has insisted he does not plan on leaving the club in the foreseeable future, despite reports of interest from both Chelsea and Paris Saint-Germain.",
                    sourceIconUrl: "https://images.fotmob.com/image_resources/news/fotmob.png",
                    pageURL: "https://www.fotmob.com/embed/news/01hr4g5xs6dm/rafael-leao-definitive-response-chelsea-psg-transfer"
                },
            ],
        }
    },
    components: {
        NewsItem,
        TimeStamp, 
        NewsItemFooter
    }
}
</script>

<template>
    <header class="WorldNewsHeader">
        <h1>World News</h1>
    </header>
    <div class="layout">
        <div class="featuredArticle">
            <div class="featuredImage">
                <img :src="featuredArticle.imageUrl" alt="featured article image" />
            </div>
            <div class="featuredArticleText">
                <h3>{{ featuredArticle.title }}</h3>
                <NewsItemFooter :article="featuredArticle" />
            </div>
        </div>
        <div class="articleGrid">
            <NewsItem v-for="article in articles" :newsItem="article" :key="article.title" />
        </div>
    </div>
</template>

<style scoped>
.WorldNewsHeader {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    margin: 0px 30px;
}
.featuredArticle {
    cursor: pointer;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 1fr;
    padding: 0px 30px;
    position: relative;
}
.featuredImage {
    width: 100%;
    height: 100%;
    max-width: 640px;
}
.featuredImage>img {
    /* needs to also specify child to resize */
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.featuredArticleText {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
    background: var(--GlobalColorScheme-Background-background2);
    height: 100%;
    width: 100%;
    flex-direction: column;
    gap: 24px;
    padding: 20px;
}
.articleGrid {
    margin-top: 48px;
    padding: 0px 30px;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 40px 24px;
    -webkit-box-align: start;
    align-items: start;
}
</style>