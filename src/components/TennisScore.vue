<template>
	<div class="flex flex-col gap-4 items-center p-4 bg-white text-slate-600 rounded-xl shadow-md">
		<section class="flex justify-center items-center gap-6 lg:gap-16 lg:mx-12 my-3 lg:my-6">
			<section class="flex flex-col items-center gap-4">
				<div class="font-bold flex items-center justify-center bg-blue-300 rounded-full w-20 lg:w-24 h-20 lg:h-24"><h1 class="bg-white rounded-full shadow-md w-16 lg:w-20 h-16 lg:h-20 flex items-center justify-center">{{ t1 }}</h1></div>
				<h2 class="hidden lg:block">{{ t1 }}</h2>
			</section>
			<section class="flex flex-col items-center lg:gap-2">
				<section class="flex gap-2 text-xl lg:text-2xl text-green-500">
					<span>{{ score }}</span>
				</section>
				<section class="flex gap-2 text-md lg:text-xl">
					<span>{{ set }}</span>
				</section>
			</section>
			<section class="flex flex-col items-center gap-4">
				<div class="font-bold flex items-center justify-center bg-red-300 rounded-full w-20 lg:w-24 h-20 lg:h-24"><h1 class="bg-white rounded-full shadow-md w-16 lg:w-20 h-16 lg:h-20 flex items-center justify-center">{{ t2 }}</h1></div>
				<h2 class="hidden lg:block">{{ t2 }}</h2>
			</section>
		</section>
	</div>
</template>

<script>
export default {
	props: {
		t1: String,
		t2: String,
		score: String,
		set: String
	}
}
</script>