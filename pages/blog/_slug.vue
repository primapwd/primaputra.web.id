<template>
    <div class="post">
        <h1>{{ article.title }}</h1>
        <!-- <TableOfContent :toc="article.toc"></TableOfContent> -->
        <v-img 
            v-if="article.image"
            :src="article.image"
            :alt="article.title"
        ></v-img>
        <nuxt-content :document="article"></nuxt-content>
    </div>
</template>
<script>
import Prism from "~/plugins/prism";
import { TableOfContent } from "~/components/TableOfContent.vue";

export default {
    mounted() {
        Prism.highlightAll();
    },
    async asyncData({ $content, params, error }) {
        try {
            const [article ] = await $content({ deep: true })
                .where({ dir: `/${params.slug}` })
                .fetch();

            console.log(article);

            const moreStories = await $content({ deep: true })
                .only(['title', 'image', 'path'])
                .where({ title: { $ne: article.title } })
                .sortBy('date', 'desc')
                .limit(3)
                .fetch();
            
            return { article, moreStories }
        } catch (err) {
            error({
                statusCode: 404,
                message: 'Page could not be found',
            });
        }
    },
}
</script>