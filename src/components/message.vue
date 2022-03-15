<script setup lang="ts">
	import { useMessage } from 'naive-ui'
	// 信息通知
	window.$message = useMessage()
</script>

<template>
	<!-- 信息中间层 -->
	<slot />
</template>
