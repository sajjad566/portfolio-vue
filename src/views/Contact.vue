<template>
    <div class="main-container">
        
        <Header />

        <div class="breadcrumb-area">
            <div class="container">
                <div class="row">
                    <div class="col">
                        <div class="breadcrumb-wrap text-center">
                            <div class="section-title">
                                <span class="water-text">Contact Me</span>
                                <h1 class="title">Contact Me</h1>
                            </div>
                            <nav aria-label="breadcrumb">
                                <ul class="breadcrumb">
                                    <li class="breadcrumb-item">
                                        <router-link to="/">Home</router-link>
                                    </li>
                                    <li class="breadcrumb-item active" aria-current="page">
                                        Contact Us
                                    </li>
                                </ul>
                            </nav>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- <div class="google-map section-padding pb-0">
            <div class="container">
                <GoogleMap />
            </div>
        </div> -->

        <ContactUs />

        <OffCanvasMobileMenu />

        <Footer />

        <BackToTop />

    </div>
</template>

<script>
    import Header from '@/components/Header';
    import GoogleMap from '@/components/GoogleMap';
    import ContactUs from '@/components/ContactUs';
    import OffCanvasMobileMenu from '@/components/OffCanvasMobileMenu';
    import Footer from '@/components/Footer';
    import BackToTop from '@/components/BackToTop';
    
    export default {
        components: {
            Header,
            GoogleMap,
            ContactUs,
            OffCanvasMobileMenu,
            Footer,
            BackToTop
        },
        metaInfo: {
            title: 'Contact Me',
            htmlAttrs: {
                lang: 'en',
                amp: true
            }
        }
    }
</script>
