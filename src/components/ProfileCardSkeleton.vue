<template>
	<div class="profile-card">
		<div class="profile-image">
			<img />
		</div>
		<div class="profile-info">
			<span />
			<h3 />
			<p />
		</div>
	</div>
</template>

<style scoped>
.profile-image img {
	width: 100%;
	padding-top: 100%;
	animation: pulse-bg 1s infinite;
}
.profile-info span {
	width: 100%;
	height: 16px;
	display: block;
	animation: pulse-bg 1s infinite;
}
.profile-info h3 {
	width: 250px;
	height: 24px;
	animation: pulse-bg 1s infinite;
}
.profile-info p {
	width: 80%;
	height: 16px;
	animation: pulse-bg 1s infinite;
}
@keyframes pulse-bg {
	0% {
		background-color: #eee;
	}
	50% {
		background-color: #eaeaea;
	}
	100% {
		background-color: #eee;
	}
}
</style>
