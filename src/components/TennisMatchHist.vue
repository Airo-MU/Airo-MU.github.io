<template>
	<div class="flex flex-col h-scores p-6 lg:p-8 border-r-2 border-slate-200">
		<section class="flex flex-col w-matches gap-6">
			<h1 class="font-bold">{{ event }} Matches</h1>
			<div class="grid gap-4 grid-cols-1 justify-items-center py-3 border-x-2 border-t-2 rounded-t-xl text-lg" style="background-color: #FFC758; border-color: #FFC758;">
				<div class="font-bold">Previous Matches</div>
			</div>
		</section>
		<div class="flex flex-col border-2 border-slate-200 bg-slate-100 rounded-b-xl divide-y-2 divide-dashed w-matches h-matches overflow-y-scroll">
			<section v-for="i in tennis" :key="i">
				<div class="grid gap-4 grid-cols-3 justify-items-center text-slate-600 py-2">
					<div class="font-bold">{{ i.team_1 }}</div>
					<section class="flex gap-2 text-xs lg:text-sm">
						<span>{{ i.set }}</span>
					</section>
					<div class="font-bold">{{ i.team_2 }}</div>
				</div>
			</section>
		</div>
	</div>
</template>

<script>
import axios from "axios"

export default {
	data() {
		return {
			tennis: []
		}
	},
	props: {
		event: String
	},
	created() {
		axios
			.get("https://raw.githubusercontent.com/Airo-MU/matches/master/tennis/tennis.json")
			.then((res) => {
				this.tennis = res.data
			})
	}
}
</script>

<style>
::-webkit-scrollbar {
	width: 0px;
	background: transparent;
}

.w-matches {
	width: 320px;
}

.h-matches {
	max-height: 506px;
}
</style>