<template>
    <div class="footer">
        <a href="https://beian.miit.gov.cn/" target="_blank">赣ICP备2023005697号-1</a>
    </div>
</template>

<script>
import {defineComponent, ref, watch} from 'vue';
import store from "@/store";
import router from '@/router'

export default defineComponent({
    name: "the-bottom-view",
    setup() {
        let member = store.state.member;
        const selectedKeys = ref([]);

        watch(() => router.currentRoute.value.path, (newValue) => {
            console.log('watch', newValue);
            selectedKeys.value = [];
            selectedKeys.value.push(newValue);
        }, {immediate: true});
        return {
            member,
            selectedKeys
        };
    },
});

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    background-color: #f0f0f0;
    padding: 10px;
    text-align: center;
    font-size: 12px;
}
</style>
