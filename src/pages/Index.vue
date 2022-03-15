<script setup lang="ts">
	import { useNotice } from '~/composables/useNotice'

	const { t, locale } = useI18n()
	const { isDark, toggleDark } = useDarks()

	const toggleLocale = () => {
		locale.value = locale.value === 'zh-CN' ? 'en' : 'zh-CN'
	}
</script>

<template>
	<div class="m-6">Hello，This is the tov template！！</div>
	<div class="cursor-pointer m-6" @click="toggleDark()"
		>light: {{ isDark }} click me!!</div
	>

	<div class="cursor-pointer m-6" @click="toggleLocale()"
		>language: {{ t('index') }} click me!!</div
	>

	<n-button
		class="ml-6"
		@click="useNotice('你好，这是一个全局的notice')"
		>NAIVE-UI</n-button
	>
</template>
