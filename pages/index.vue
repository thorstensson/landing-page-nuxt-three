<script setup lang="ts">

definePageMeta({
    layout: 'default'
});

const scrollConfig = reactive({
    text: '                        Swedish multidisciplinary developer. Sprinting towards reboot. Freelancing Nuxt Developer @ Solume AI. Based: Barcelona / London. Looking for perm Vue role EU / Spain, open to talks...',
})

// leaving this in here as I was thinking of switching components on a setTimeOut
const compName = shallowRef(resolveComponent('ThreeShaderPoints'))

</script>

<template>
    <div class="page-wrapper">
        <component :is="compName" />
        <UITextScroller :text="scrollConfig.text" />
    </div>
</template>

<style lang="scss" scoped>
.page-wrapper {
    height: 100vh;
    overflow-y: hidden;
}
</style>