<script>
import AboutClientSingle from './AboutClientSingle.vue';

export default {
	components: {
		AboutClientSingle,
	},
	data: () => {
		return {
			clientsHeading: 'Some of the technologies I have worked with',
			clients: [
				{
					id: 1,
					title: 'JavaScript',
					img: require('@/assets/images/brands/jscript.png'),
				},
				{
					id: 2,
					title: 'Vue.js',
					img: require('@/assets/images/brands/vuejs.png'),
				},
				{
					id: 3,
					title: 'Tailwind CSS',
					img: require('@/assets/images/brands/tailwind.png'),
				},
				{
					id: 4,
					title: 'jQuery',
					img: require('@/assets/images/brands/jquery (1).png'),
				},
				{
					id: 5,
					title: 'PHP',
					img: require('@/assets/images/brands/php.png'),
				},
				{
					id: 6,
					title: 'R Programming',
					img: require('@/assets/images/brands/rlanguage.jpg'),
				},
				{
					id: 7,
					title: 'CANON',
					img: require('@/assets/images/brands/python.png'),
				},
				// {
				// 	id: 7,
				// 	title: 'PUMA',
				// 	img: require('@/assets/images/brands/puma_gray.png'),
				// },
			],
		};
	},
};
</script>

<template>
	<div class="mt-10 sm:mt-20">
		<p
			class="font-general-medium text-2xl sm:text-3xl text-primary-dark dark:text-primary-light"
		>
			{{ clientsHeading }}
		</p>
		<div class="grid grid-cols-2 sm:grid-cols-4 mt-10 sm:mt-14 gap-2">
			<AboutClientSingle
				v-for="client in clients"
				:key="client.id"
				:client="client"
			/>
		</div>
	</div>
</template>
