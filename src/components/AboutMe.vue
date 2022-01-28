<template>
    <section class="about-us-area section-padding bg-color-light">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title text-center">
                        <span class="water-text">{{ data.about.sectionTitleWaterText }}</span>
                        <h2 class="title">{{ data.about.sectionTitle }}</h2>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-10 offset-lg-1">
                    <div class="about-us">
                        <div class="about-us__content text-center">
                            <p>{{ data.about.aboutMe }}</p>
                            <div class="signature">
                                <img src="/img/logo/sjd-10.png" alt="signature">
                            </div>
                            <div class="social-link">
                                <a :href="social.link" target="_blank" v-for="social in data.socials" :key="social.id">
                                    <i :class="social.icon"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import data from '../data/about.json';
    export default {
        data () {
            return {
                data
            }
        }
    };
</script>

<style lang="scss">
    @import '../assets/scss/_variables.scss';

    .about-us {
        &__content {
            padding: 0 40px;
            // res
            @media #{$sm-device}{
                padding: 0;
            }
            p {
                color: #bbb;
                font-size: 16px;
            }
            .signature {
                max-width: 170px;
                margin: 30px auto 0;
            }
            .social-link {
                margin-top: 20px;
                display: inline-block;
                position: relative;
                padding: 0 30px;
                &:before,
                &:after {
                    top: 50%;
                    left: -50px;
                    width: 60px;
                    height: 1px;
                    content: "";
                    position: absolute;
                    background-color: $theme-color-secondary;
                    transform: translateY(-50%);
                }
                &:after {
                    left: auto;
                    right: -50px;
                }
                a {
                    font-size: 20px;
                    color: $theme-color-secondary;
                    margin-right: 20px;
                    &:hover {
                        color: $theme-color-primary;
                    }
                    &:last-child {
                        margin-right: 0;
                    }
                }
            }
            .download-btn {
                display: block;
                font-size: 18px;
                margin: auto;
                margin-top: 15px;
                line-height: 1;
                color: $theme-color-secondary;
                span {
                    color: $theme-color-primary;
                    text-decoration: underline;
                }
            }
        }
    }
</style>