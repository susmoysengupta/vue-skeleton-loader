<template>
	<div class="profile-card">
		<div class="profile-image">
			<img :src="userData.pic" alt="Pic" />
		</div>
		<div class="profile-info">
			<span> Written By </span>
			<h3>{{ userData.name }}</h3>
			<p>{{ userData.bio }}</p>
		</div>
	</div>
</template>

<script>
import { ref } from "vue";

const loadUserData = async () => {
	return new Promise((resolve) => {
		setTimeout(() => {
			resolve({
				name: "Susmoy Sen Gupta",
				pic: "https://raw.githubusercontent.com/SusmoySenGupta/readme-contents/main/my-images/my-image-01.jpg",
				bio: "I am a Full Stack Web Developer",
			});
		}, 2000);
	});
};

export default {
	async setup() {
		const userData = ref(await loadUserData());

		return {
			userData,
		};
	},
};
</script>


