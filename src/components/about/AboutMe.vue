<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					bio:
						'I am passionate about and highly motivated by the opportunities in website development and data analytics. These fields ignite my creativity and analytical thinking, driving me to continually learn and grow. In website development, I thrive on creating engaging, user-friendly, and efficient web experiences. I enjoy the process of transforming ideas into functional websites, ensuring they are aesthetically pleasing and technically sound. In the realm of data analytics, I am fascinated by the ability to uncover insights from data. I enjoy using tools and techniques to analyze data, identify trends, and make data-driven decisions that can drive business strategy and efficiency.',
				},
				{
					id: 2,
					bio:
						' Additionally, I am exploring application development with the Flutter framework. This cross-platform technology allows me to create natively compiled applications for mobile, web, and desktop from a single codebase, which is both efficient and exciting. I am also delving into backend development using Node.js, a powerful JavaScript runtime that enables server-side scripting. This allows me to build scalable and high-performance applications, further enhancing my full-stack development capabilities.',
				},
			],
		};
	},
};
</script>

<template>
	<div class="block sm:flex sm:gap-10 mt-10 sm:mt-20">
		<!-- About profile image -->
		<div class="w-full sm:w-1/4 mb-7 sm:mb-0">
			<img
				src="@/assets/images/profile2.jpg"
				class="rounded-xl w-96"
				alt=""
			/>
		</div>

		<!-- About details -->
		<div class="w-full sm:w-3/4 text-left">
			<p
				v-for="bio in bios"
				:key="bio.id"
				class="font-general-regular mb-4 text-ternary-dark dark:text-ternary-light text-lg text-justify"
			>
				{{ bio.bio }}
			</p>
		</div>
	</div>
</template>
