<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of list" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "HomeSwiper",
    data () {
        return {
            swiperOption: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: "0001",
                imgUrl: '//img1.qunarzz.com/vc/1d/d5/dc/bfb1990e14a1fdb082cf817657.jpg'
            }, {
                id: "0002",
                imgUrl: '//img1.qunarzz.com/vc/f5/10/9c/b647d3ee724a720ce0fa6101f0.jpg'
            }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #ffffff
    .wrapper 
        overflow: hidden
        width: 100%
        height: 0
        padding-bottom: 31.25%
        background: #eee
        .swiper-img 
            width: 100%

</style>
