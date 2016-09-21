<template>
    <navbar placement="top" type="default">
        <!-- Brand as slot -->
        <a slot="brand" href="/" title="Home" class="navbar-brand">明其道不计其功</a>
        <ul class="nav navbar-nav">
            <li>
                <a v-link="{path: '/3'}">数据</a>
            </li>
            <li>
                <a v-link="{path: '/blog'}">博客</a>
            </li>
            <li>
                <a v-link="{path: '/movie'}">电影</a>
            </li>
            <li>
                <a v-link="{path: '/smzdm'}">好价</a>
            </li>
        </ul>
    </navbar>
    <router-view>
    </router-view>
</template>
<script>
import {
    navbar,
    dropdown
} from 'vue-strap'

export default {
    data() {
            return {

            }
        },
        components: {
            navbar,
            dropdown
        }
}
</script>
