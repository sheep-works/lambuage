<template>
    <v-img src="/pict/lambuage.png" height="50px" position="left top" @click="navigateToTop" />
</template>

<script setup lang="ts">
const router = useRouter()

const navigateToTop = () => {
    router.push("/")
}
</script>
