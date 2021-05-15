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

<style>
.profile-card {
  width: 100%;
  max-width: 700px;
  min-height: 180px;
  background: white;
  margin: 0 auto;
  padding: 30px;
  box-sizing: border-box;
  overflow: hidden;
  border-radius: 20px;
}
.profile-image {
  width: 10%;
  float: left;
}
.profile-image img {
  width: 100%;
  height: auto;
  border-radius: 50%;
  border: 5px solid #42b883;
  padding: 5px;
}
.profile-info {
  width: 85%;
  float: right;
}
.profile-info span {
  text-transform: uppercase;
  color: #777;
  letter-spacing: 3px;
}
.profile-info h3 {
  margin: 10px 0;
  font-size: 1.5em;
  color: #222;
}
.profile-info p {
  line-height: 140%;
  color: #777;
}
</style>
