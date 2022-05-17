<template>
	<div class="flex flex-col gap-4 items-center p-4 bg-white text-slate-600 rounded-xl shadow-md">
		<section class="flex justify-center items-center gap-6 lg:gap-16 lg:mx-12 my-3 lg:my-6">
			<section class="flex flex-col items-center gap-4">
				<div class="flex items-center justify-center bg-blue-300 rounded-full w-20 lg:w-24 h-20 lg:h-24"><h1 class="bg-white rounded-full shadow-md w-16 lg:w-20 h-16 lg:h-20 flex items-center justify-center text-xs lg:text-base">{{ t1 }}</h1></div>
				<span class="text-xl lg:text-2xl text-green-500 font-bold">{{ score1 }}</span>
				<h2 class="font-bold">{{ t1 }}</h2>
			</section>
			<section class="flex flex-col items-center lg:gap-2">
				<section>
					<h2 class="flex text-md lg:text-xl flex-col items-center font-bold"><span class="text-xl lg:text-4xl">{{ overs }}</span><span>overs</span></h2>
				</section>
			</section>
			<section class="flex flex-col items-center gap-4">
				<div class="flex items-center justify-center bg-red-300 rounded-full w-20 lg:w-24 h-20 lg:h-24"><h1 class="bg-white rounded-full shadow-md w-16 lg:w-20 h-16 lg:h-20 flex items-center justify-center text-xs lg:text-base">{{ t2 }}</h1></div>
				<span class="text-xl lg:text-2xl text-green-500 font-bold">{{ score2 }}</span>
				<h2 class="font-bold">{{ t2 }}</h2>
			</section>
		</section>
	</div>
	<h1 class="font-bold">{{ winner }}</h1>
</template>

<script>
export default {
	props: {
		t1: String,
		t2: String,
		score1: String,
		score2: String,
		overs: String,
		winner: String
	}
}
</script>