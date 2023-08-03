<template>
    <a-layout id="components-layout-demo-top-side-2">
        <the-header-view></the-header-view>
        <a-layout>
            <the-sider-view></the-sider-view>
            <a-layout-content
                    :style="{ background: '#fff', padding: '24px', margin: 0, minHeight: '280px' }"
            >
                <router-view></router-view>
            </a-layout-content>
        </a-layout>
        <the-bottom-view></the-bottom-view>
    </a-layout>
</template>
<script>
import {defineComponent} from 'vue';
import TheHeaderView from "@/components/the-header";
import TheSiderView from "@/components/the-sider";
import TheBottomView from "@/components/the-bottom";

export default defineComponent({
    components: {
        TheSiderView,
        TheHeaderView,
        TheBottomView
    },
    setup() {
        return {};
    },
});
</script>
<style>

</style>
