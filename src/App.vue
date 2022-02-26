<script setup lang="ts">
import { darkTheme } from 'naive-ui'

const { isDark } = useDarks()
const theme = computed(() => isDark.value ? darkTheme : null)
</script>

<template>
    <n-config-provider :theme="theme">
        <router-view />
    </n-config-provider>
</template>