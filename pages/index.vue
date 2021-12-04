<template>
    <div class="page fill-height">
        <div class="landing">
            <v-row no-gutters class="fill-height" align="center" justify="center">
                <v-col class="left fill-height d-none d-sm-block">
                    <iframe src='https://my.spline.design/untitled-08a51b8374d1d0ca0554e5fe4c5596dc/' frameborder='0' width='100%' height='100%'></iframe>
                </v-col>
                <v-col class="right px-14 ">
                    <div class="text-right px-10 mb-7">

                        <div class="text-h2 ">
                            تاکو ئێستا ڤاکسین نەکراوی؟
                        </div>
                        <div class="my-7"></div>
                        <div class="text-span text--secondary">
                            بۆ تۆمارکردنی زانيارييەكانت لە سیستەمی تۆمارکردنى پێش وەخت بۆ کوتانی کۆڤید-19،
                            تکایە دڵنیابە لەوەی کە زانیاريیەکەت دروستە، چونکە پەیوەندیت پێوە دەکەین بۆ بەروارى وەرگرتنی ڤاکسینەکە.
                        </div>
                        <div class="my-7"></div>

                        <v-btn class="rounded-xl text-right" color="primary" large>
                            خۆت تۆمارکە
                        </v-btn>
                    </div>

                </v-col>
            </v-row>
        </div>
        <div class="whitespace"></div>
        <div class="about">
            <div class="bg">
                <v-img src="/blob.svg" height="100%" width="100%">
                </v-img>
            </div>

            <div class="content fill-height d-flex flex-column align-center justify-center">
                <v-row no-gutters class="fill-height " align="center" justify="center">
                    <v-col class="left d-none d-sm-block">
                        <v-row class="px-14 pb-7" align="end">
                            <v-col cols="4">
                                <v-img class="elevation-2" max-width="250" src="https://images.pexels.com/photos/5878503/pexels-photo-5878503.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                                </v-img>
                            </v-col>
                            <v-col cols="4">
                                <v-img class="elevation-2" max-width="250" src="https://images.pexels.com/photos/8830469/pexels-photo-8830469.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260s">
                                </v-img>
                            </v-col>
                            <v-col cols="3">
                                <v-img class="elevation-2" max-width="250" src="https://images.pexels.com/photos/3952224/pexels-photo-3952224.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260">
                                </v-img>
                            </v-col>

                        </v-row>
                    </v-col>
                    <v-col class="right">
                        <div class="text-right px-10 mb-7">

                            <div class="text-h2 ">
                                تاکو ئێستا ڤاکسین نەکراوی؟
                            </div>
                            <div class="my-7"></div>
                            <div class="text-span text--secondary">
                                بۆ تۆمارکردنی زانيارييەكانت لە سیستەمی تۆمارکردنى پێش وەخت بۆ کوتانی کۆڤید-19،
                                تکایە دڵنیابە لەوەی کە زانیاريیەکەت دروستە، چونکە پەیوەندیت پێوە دەکەین بۆ بەروارى وەرگرتنی ڤاکسینەکە.
                            </div>
                            <div class="my-7"></div>

                            <v-btn class="rounded-xl text-right" color="primary" large>
                                خۆت تۆمارکە
                            </v-btn>
                        </div>
                    </v-col>
                </v-row>
            </div>

        </div>
        <div class="whitespace"></div>
        <div class="symptoms ">
            <v-row align="center" justify="center">
                <v-col lg="3" cols="8" class="text-center ma-4 py-4 px-2 elevation-1 d-flex flex-column align-center justify-center rounded-lg" v-for="sym,i in symptoms" :key="i">
                    <v-img :src="sym.icon" height="60" max-height="60" contain></v-img>
                    <div class="ma-3"></div>
                    <div class="text-span">
                        {{sym.text}}
                    </div>
                </v-col>
            </v-row>
        </div>
        <div class="whitespace"></div>
        <div class="find-hospitals ">
            <v-row no-gutters align="center" justify="center" class="fill-height">
                <v-col cols="6"   class="fill-height d-none d-sm-block">
                    <v-img src="/hospital.jpg" height="95%"></v-img>
                </v-col>
                <v-col cols="6"  class="fill-height d-flex align-center justify-center ">
                    <v-row no-gutters align="center" justify="start" class="px-5">
                        <v-col v-for="i in 4" :key="i" lg="5" cols="7" md="5" class="ma-3">
                            <v-card width="300" height="250">
                                <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12984.680271576131!2d45.4659816!3d35.5495018!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x53a6b8021f30f030!2sFaruk%20Medical%20City!5e0!3m2!1sen!2siq!4v1638566782817!5m2!1sen!2siq" height="250" width="300" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                            </v-card>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </div>
    </div>
</template>

<script>

export default {
    components: {

    },

    data() {
        return {
            symptoms: [
                { text: 'کۆکەیەکی زۆری بەردەوام', icon: '/cough.png' },
                { text: 'تایەکی زۆر', icon: '/pcr-test.png' },
                { text: 'بێزاری و بێتاقەتی', icon: '/tiredness.png' },
                { text: 'لەدەسدانی تام و بۆن', icon: '/snot.png' },
                { text: 'ئازار و سەرئێشە', icon: '/sick.png' },
                { text: 'هەناسەدانی قورس', icon: 'breathing.png' }
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
.whitespace {
    height: 20vh;
}
.page {
    width: 100%;
    .landing {
        height: 100vh;
        width: 100%;
        background-attachment: fixed;
        position: relative;
        .left {
            // position: absolute;
            // z-index: 1;
        }
        .right {
            // position: absolute;
            // z-index: 2;
            // background: rgba($color: #000000, $alpha: 0.08);
        }
    }
    .about {
        height: 140vh;
        width: 100%;
        position: relative;

        .bg {
            position: absolute;
            z-index: 1;
            width: 100%;
            height: 100%;
        }
        .content {
            position: absolute;
            z-index: 2;

            width: 100%;
        }
    }

    .symptoms {
        min-height: 60vh;
        max-height: 100%;
        width: 100%;
    }
    .find-hospitals {
        height: 100vh;
        width: 100%;
        background: #e63946;
    }
}
@media only screen and (max-width: 600px) {
    .find-hospitals {
        height: unset !important;
        min-height: 100vh;
        max-height: 100%;
        width: 100%;
        background: #e63946;
        padding-top: 10vh;
        padding-bottom: 10vh;
    }
}
</style>