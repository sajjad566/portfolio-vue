<template>
    <div class="portfolio-item">
        <div class="portfolio-item__thumb">
            <a :href="portfolio.link" target="_blank">
                <v-lazy-image :src="portfolio.image" alt="portfolio image" />
            </a>
        </div>
        <div class="portfolio-item__content">
            <h4 class="portfolio-title">
                <a :href="portfolio.link" target="_blank">{{ portfolio.title }}</a>
            </h4>
            <p>{{ portfolio.desc }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['portfolio']
    };
</script>