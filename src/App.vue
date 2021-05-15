<template>
	<suspense>
		<template #default>
			<ProfileCard></ProfileCard>
		</template>
		<template #fallback>
			<ProfileCardSkeleton />
		</template>
	</suspense>
</template>

<script setup>
import ProfileCard from "./components/ProfileCard.vue";
import ProfileCardSkeleton from "./components/ProfileCardSkeleton.vue";
</script>

<style>
html,
body {
	background-color: #eee;
}
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
}
</style>
