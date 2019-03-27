<template>
<div>
<detail-banner></detail-banner>
<detail-header></detail-header>
<div class='content'>
    <detail-list :list = "list"></detail-list>
</div>
</div>
</template>

<script>
import DetailBanner from './components/Banner.vue'
import DetailHeader from './components/Header.vue'
import DetailList from './components/List.vue'
import axios from 'axios'
export default {
    name: 'Detail',
    components: {
        DetailBanner,
        DetailHeader,
        DetailList
    },
    methods: {
        getDetailInfo() {
            axios.get('/api/detail.json?id=' , {
                params: {
                    id: this.$route.params.id
                }
            }).then(this.getDetailDataSucc).fail(console.log('oops'))
        }, 

        getDetailDataSucc (res) {
            res = res.data
            if (ret && res.data) {
                const data = res.data
            }
        }
    },
    mounted () {
        this.getDetailInfo()
    },
    data () {
        return {
            list: [
                {
                    title: 'Adult',
                    children: [
                        {
                            title: "Day Tour",
                            children: [
                                {
                                    title: "Day Tour - Public Holiday"
                                }
                            ]
                        },
                        {
                            title: "Day Tour + Lunch"
                        }
                    ]
                    },
                {title: 'Student'},
                {title: 'Concession'},
                {title: 'Family Pack'}
            ]
        }
    }
}
</script>

<style scoped lang="stylus">
  .content
    height: 50rem
</style>
