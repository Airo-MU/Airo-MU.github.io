<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import NavBar from './components/NavBar.vue';
import CricketMatchHist from './components/CricketMatchHist.vue';
import ScoreCard from './components/ScoreCard.vue';
import CricketScore from './components/CricketScore.vue';
import TennisScore from './components/TennisScore.vue';
import TennisMatchHist from './components/TennisMatchHist.vue';
</script>

<template>
	<nav class="fixed z-50 flex flex-col gap-8 h-screen p-4 border-r-2 bg-white border-slate-200 overflow-y-scroll lg:overflow-hidden" :class="{'w-side': expand, 'w-16': !expand}">
		<button class="ml-1" @click="expand = !expand">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M21 15.61L19.59 17L14.58 12L19.59 7L21 8.39L17.44 12L21 15.61ZM3 6H16V8H3V6ZM3 13V11H13V13H3ZM3 18V16H16V18H3Z" fill="black"/>
			</svg>
		</button>
		<ul class="ml-1 flex gap-6 flex-col text-slate-500">
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[0])">
			<div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': cricket}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M14.3398 17.77L15.7498 16.36L19.9998 20.58L18.5598 22L14.3398 17.77ZM18.4998 2C19.428 2 20.3183 2.36875 20.9746 3.02513C21.631 3.6815 21.9998 4.57174 21.9998 5.5C21.9998 6.42826 21.631 7.3185 20.9746 7.97487C20.3183 8.63125 19.428 9 18.4998 9C17.5715 9 16.6813 8.63125 16.0249 7.97487C15.3685 7.3185 14.9998 6.42826 14.9998 5.5C14.9998 4.57174 15.3685 3.6815 16.0249 3.02513C16.6813 2.36875 17.5715 2 18.4998 2V2ZM2.23977 7.11L5.06977 4.28C5.45977 3.89 6.08977 3.89 6.49977 4.28L14.9698 12.77C15.3598 13.16 15.3598 13.79 14.9698 14.18L12.1398 17C11.7498 17.4 11.1198 17.4 10.7198 17L2.23977 8.53C1.84977 8.13 1.84977 7.5 2.23977 7.11Z" />
				</svg>
			</div><h2>{{sportname[0]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[1])">
			<div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': basketball}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
					<path d="M2.34 14.6301C2.94 14.4101 3.56 14.3001 4.22 14.3001C5.56 14.3001 6.73 14.7201 7.73 15.5601L4.59 18.7001C3.53 17.5001 2.78 16.1301 2.34 14.6301ZM15.56 9.80008C17.53 11.2701 19.66 11.6301 21.94 10.8801C21.97 11.0901 22 11.4701 22 12.0001C22 13.0301 21.75 14.1801 21.28 15.4501C20.81 16.7101 20.23 17.7301 19.55 18.5001L13.22 12.1901L15.56 9.80008ZM8.77 16.6401C9.83 18.1701 10.05 19.8401 9.42 21.6601C8 21.2501 6.73 20.6101 5.67 19.7301L8.77 16.6401ZM12.19 13.2201L18.5 19.5501C16.33 21.4501 13.78 22.2501 10.88 21.9401C11.09 21.2801 11.2 20.5601 11.2 19.7801C11.2 19.1601 11.06 18.4301 10.78 17.6001C10.5 16.7701 10.17 16.0901 9.8 15.5601L12.19 13.2201ZM8.81 14.5001C7.88 13.6701 6.8 13.1501 5.58 12.9101C4.36 12.6801 3.19 12.7501 2.06 13.1301C2.03 12.9101 2 12.5301 2 12.0001C2 10.9701 2.25 9.82008 2.72 8.55008C3.19 7.29008 3.77 6.27008 4.45 5.50008L11.11 12.1901L8.81 14.5001ZM15.56 7.73008C14.22 6.08008 13.91 4.28008 14.63 2.34008C15.25 2.50008 15.96 2.80008 16.76 3.26008C17.55 3.71008 18.2 4.16008 18.7 4.59008L15.56 7.73008ZM21.66 9.38008C21.06 9.59008 20.44 9.70008 19.78 9.70008C18.69 9.70008 17.64 9.38008 16.64 8.72008L19.73 5.67008C20.61 6.77008 21.25 8.00008 21.66 9.38008ZM12.19 11.1101L5.5 4.45008C7.67 2.55008 10.22 1.75008 13.13 2.06008C12.91 2.72008 12.8 3.44008 12.8 4.22008C12.8 4.94008 12.96 5.75008 13.29 6.66008C13.62 7.56008 14 8.28008 14.5 8.81008L12.19 11.1101Z" />
				</svg>
			</div><h2>{{sportname[1]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[2])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': badminton}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M12.3 2.00004C11.33 2.03004 10.58 2.84004 10.61 3.80004C10.62 4.04004 10.67 4.27004 10.77 4.50004L11.06 5.14004C11.1 5.27004 11.03 5.41004 10.89 5.45004C10.8 5.50004 10.7 5.45004 10.63 5.37004L10.21 4.82004C9.88 4.40004 9.38 4.14004 8.85 4.13004C7.88 4.11004 7.08 4.88004 7.06 5.84004C7.05 6.26004 7.19 6.66004 7.45 7.00004L7.87 7.50004H7.88C7.96 7.63004 7.93 7.79004 7.82 7.87004C7.73 7.94004 7.61 7.94004 7.53 7.87004L7 7.45004C6.66 7.19004 6.25 7.05004 5.84 7.06004C4.88 7.08004 4.11 7.88004 4.13 8.85004C4.14 9.38004 4.4 9.88004 4.82 10.21L5.39 10.65C5.5 10.75 5.5 10.91 5.38 11C5.31 11.07 5.21 11.09 5.12 11.05H5.11L4.5 10.77C4.27 10.68 4.04 10.62 3.8 10.61C2.84 10.58 2.03 11.34 2 12.31C2 13.03 2.4 13.69 3.06 13.97L14.45 19.04L19.04 14.45L13.97 3.06004C13.69 2.39004 13 1.97004 12.3 2.00004ZM13.13 6.10004C13.55 6.09004 13.93 6.33004 14.09 6.71004L17.14 13.55L13.19 9.61004L12.26 7.50004C11.96 6.87004 12.42 6.12004 13.13 6.10004ZM9.85 8.85004C10.12 8.85004 10.37 8.95004 10.56 9.15004L15.37 13.96C15.77 14.34 15.78 14.97 15.4 15.37C15 15.77 14.38 15.78 13.96 15.37L9.15 10.56C8.75 10.18 8.74 9.54004 9.13 9.15004C9.32 8.95004 9.58 8.85004 9.85 8.85004ZM7.13 12.17C7.26 12.17 7.4 12.21 7.5 12.26L9.63 13.2L13.57 17.14L6.71 14.09C5.69 13.65 6.03 12.14 7.13 12.17ZM20.28 16.04L16.04 20.28L16.89 21.13C17.65 21.88 18.75 22.17 19.78 21.9C20.81 21.62 21.62 20.81 21.9 19.78C22.17 18.75 21.88 17.65 21.13 16.89L20.28 16.04Z" />
</svg>
			</div><h2>{{sportname[2]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[3])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': football}" width="25" height="25" viewBox="0 0 25 25" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M16.9378 17.1591L16.1378 15.7991L17.5978 11.4291L19.0078 10.9591L20.0078 11.7091C20.0078 11.7391 20.0078 11.7891 20.0078 11.8491C20.0078 11.9191 20.0378 11.9791 20.0378 12.0391C20.0378 14.0091 19.3778 15.7491 18.0678 17.2491L16.9378 17.1591ZM9.75781 15.0391L8.38781 11.0091L12.0078 8.46906L15.6278 11.0091L14.2578 15.0391H9.75781ZM12.0078 20.0691C11.1278 20.0691 10.2978 19.9291 9.50781 19.6491L8.81781 18.1391L9.47781 17.0391H14.5878L15.1978 18.1391L14.5078 19.6491C13.7178 19.9291 12.8878 20.0691 12.0078 20.0691ZM5.94781 17.2491C5.41781 16.6291 4.95781 15.7991 4.56781 14.7891C4.17781 13.7691 3.97781 12.8491 3.97781 12.0391C3.97781 11.9791 4.00781 11.9191 4.00781 11.8491C4.00781 11.7891 4.00781 11.7391 4.00781 11.7091L5.00781 10.9591L6.41781 11.4291L7.87781 15.7991L7.07781 17.1591L5.94781 17.2491ZM11.0078 5.32906V6.72906L7.00781 9.49906L5.66781 9.07906L5.24781 7.71906C5.68781 7.03906 6.33781 6.35906 7.19781 5.69906C8.05781 5.03906 8.87781 4.60906 9.65781 4.38906L11.0078 5.32906ZM14.3578 4.38906C15.1378 4.60906 15.9578 5.03906 16.8178 5.69906C17.6778 6.35906 18.3278 7.03906 18.7678 7.71906L18.3478 9.07906L17.0078 9.50906L13.0078 6.73906V5.32906L14.3578 4.38906ZM4.93781 4.96906C3.00781 6.92906 2.00781 9.28906 2.00781 12.0391C2.00781 14.7891 3.00781 17.1491 4.93781 19.1091C6.86781 21.0691 9.25781 22.0391 12.0078 22.0391C14.7578 22.0391 17.1178 21.0391 19.0778 19.1091C21.0378 17.1791 22.0078 14.7891 22.0078 12.0391C22.0078 9.28906 21.0078 6.92906 19.0778 4.96906C17.1478 3.00906 14.7578 2.03906 12.0078 2.03906C9.25781 2.03906 6.89781 3.03906 4.93781 4.96906Z" />
</svg>
			</div><h2>{{sportname[3]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[4])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': volleyball}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M19.04 4.85C17.34 3.2 15.33 2.25 13 2V5.62L22 10.8C21.72 8.5 20.73 6.5 19.04 4.85ZM12 22C15.44 22 18.16 20.62 20.17 17.86L17.06 16L8.07 21.2C9.32 21.73 10.64 22 12 22ZM13 11.41L21.15 16.07C21.59 15.13 21.88 14.14 22 13.11L13 7.93V11.41ZM3.88 17.81C4.54 18.72 5.26 19.46 6.05 20L15.04 14.9L12 13.15L3.88 17.81ZM11.04 2C10 2.09 9 2.36 8 2.8V13.15L11.04 11.41V2ZM2 12C2 13.39 2.3 14.77 2.89 16.12L6 14.28V4C3.33 6 2 8.65 2 12Z" />
</svg>
			</div><h2>{{sportname[4]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[5])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': throwball}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M12 2C14.5 2 16.75 2.9 18.5 4.4C16.36 6.23 15 8.96 15 12C15 15.04 16.36 17.77 18.5 19.6C16.75 21.1 14.5 22 12 22C9.5 22 7.25 21.1 5.5 19.6C7.64 17.77 9 15.04 9 12C9 8.96 7.64 6.23 5.5 4.4C7.25 2.9 9.5 2 12 2ZM22 12C22 14.32 21.21 16.45 19.88 18.15C18.12 16.68 17 14.47 17 12C17 9.53 18.12 7.32 19.88 5.85C21.21 7.55 22 9.68 22 12ZM2 12C2 9.68 2.79 7.55 4.12 5.85C5.88 7.32 7 9.53 7 12C7 14.47 5.88 16.68 4.12 18.15C2.79 16.45 2 14.32 2 12Z" />
</svg>
			</div><h2>{{sportname[5]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[6])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': chess}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M19.0002 22H5.00024V20H19.0002V22ZM17.0002 10C15.5802 10 14.2602 10.77 13.5502 12H13.0002V7H16.0002V5H13.0002V2H11.0002V5H8.00024V7H11.0002V12H10.4502C9.35024 10.09 6.90024 9.43 5.00024 10.54C3.07024 11.64 2.42024 14.09 3.50024 16C4.24024 17.24 5.57024 18 7.00024 18H17.0002C18.0611 18 19.0785 17.5786 19.8287 16.8284C20.5788 16.0783 21.0002 15.0609 21.0002 14C21.0002 12.9391 20.5788 11.9217 19.8287 11.1716C19.0785 10.4214 18.0611 10 17.0002 10V10Z" />
</svg>
			</div><h2>{{sportname[6]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[7])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': tt}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M18.5 14C19.9 14 21 15.1 21 16.5C21 17.9 19.9 19 18.5 19C17.1 19 16 17.9 16 16.5C16 15.1 17.1 14 18.5 14ZM7 15C7 15 8 16 8 17V20.5C8 21.3 8.7 22 9.5 22C10.3 22 11 21.3 11 20.5V17C11 16 12 15 12 15H7ZM8 14H11C11 14 16 14 16 9C16 4 12 2 9.5 2C7 2 3 4 3 9C3 14 8 14 8 14Z" />
</svg>
			</div><h2>{{sportname[7]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[8])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': pool}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M11 13H13V15H11V13ZM11 9H13V11H11V9ZM11 17H13C13.5304 17 14.0391 16.7893 14.4142 16.4142C14.7893 16.0391 15 15.5304 15 15V13.5C15 13.1022 14.842 12.7206 14.5607 12.4393C14.2794 12.158 13.8978 12 13.5 12C13.8978 12 14.2794 11.842 14.5607 11.5607C14.842 11.2794 15 10.8978 15 10.5V9C15 8.46957 14.7893 7.96086 14.4142 7.58579C14.0391 7.21071 13.5304 7 13 7H11C10.4696 7 9.96086 7.21071 9.58579 7.58579C9.21071 7.96086 9 8.46957 9 9V10.5C9 10.8978 9.15804 11.2794 9.43934 11.5607C9.72064 11.842 10.1022 12 10.5 12C10.1022 12 9.72064 12.158 9.43934 12.4393C9.15804 12.7206 9 13.1022 9 13.5V15C9 15.5304 9.21071 16.0391 9.58579 16.4142C9.96086 16.7893 10.4696 17 11 17ZM12 1C5.92 1 1 5.92 1 12C1 18.08 5.92 23 12 23C18.08 23 23 18.08 23 12C23 5.92 18.08 1 12 1ZM12 19C10.1435 19 8.36301 18.2625 7.05025 16.9497C5.7375 15.637 5 13.8565 5 12C5 10.1435 5.7375 8.36301 7.05025 7.05025C8.36301 5.7375 10.1435 5 12 5C13.8565 5 15.637 5.7375 16.9497 7.05025C18.2625 8.36301 19 10.1435 19 12C19 13.8565 18.2625 15.637 16.9497 16.9497C15.637 18.2625 13.8565 19 12 19V19Z" />
</svg>
			</div><h2>{{sportname[8]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[9])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': snooker}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M20.3099 16.4402L14.5399 6.47019C13.7199 5.04019 11.8899 4.55019 10.4599 5.38019C9.99991 5.64019 9.62991 6.00019 9.35991 6.47019L3.59991 16.4402C2.76991 17.8702 3.25991 19.6902 4.68991 20.5002C5.13991 20.7802 5.64991 20.9202 6.17991 20.9202H17.7299C19.3799 20.9102 20.7199 19.5702 20.7099 17.9202C20.7099 17.4002 20.5699 16.8902 20.3099 16.4402ZM5.36991 17.4302L11.1099 7.47019C11.3799 7.00019 11.9999 6.82019 12.4599 7.10019C12.6199 7.18019 12.7499 7.31019 12.8399 7.47019L18.5799 17.4302C18.8499 17.9102 18.6899 18.5002 18.2099 18.7902C18.0599 18.8802 17.8899 18.9302 17.7199 18.9302H6.20991C5.65991 18.9202 5.20991 18.4702 5.21991 17.9202C5.21991 17.7502 5.25991 17.5802 5.34991 17.4302H5.36991ZM11.9699 13.4502C10.8699 13.4502 9.99991 12.5602 9.99991 11.4602C9.99991 10.3502 10.8699 9.46019 11.9699 9.46019C12.5003 9.46019 13.0091 9.6709 13.3841 10.046C13.7592 10.421 13.9699 10.9298 13.9699 11.4602C13.9699 12.5602 13.0699 13.4502 11.9499 13.4502H11.9699ZM9.45991 17.9302C8.35991 17.9302 7.46991 17.0402 7.46991 15.9402C7.46991 14.8402 8.35991 13.9502 9.45991 13.9502C10.5599 13.9502 11.4599 14.8402 11.4599 15.9402C11.4599 17.0402 10.5599 17.9302 9.45991 17.9302ZM14.4399 17.9302C13.9129 17.9276 13.4083 17.7171 13.0357 17.3444C12.663 16.9718 12.4525 16.4672 12.4499 15.9402C12.4525 15.4132 12.663 14.9086 13.0357 14.5359C13.4083 14.1633 13.9129 13.9528 14.4399 13.9502C15.5399 13.9502 16.4399 14.8402 16.4399 15.9402C16.4399 17.0402 15.5399 17.9302 14.4399 17.9302Z" />
</svg>
			</div><h2>{{sportname[9]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[10])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': kho}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M12.0001 1V2L11.2301 1.36L7.76006 5.5L11.0001 7.5V5.16L10.7801 5L12.0001 3.56V23H14.0001V13.24L15.9301 11.31C18.5001 11.71 21.1301 10.36 22.6601 8.83L21.2401 7.41C20.1001 8.56 17.7001 9.61 16.0001 9.26L14.0001 7.24V1H12.0001ZM17.0001 4C16.4696 4 15.9609 4.21071 15.5858 4.58579C15.2108 4.96086 15.0001 5.46957 15.0001 6C15.0001 6.53043 15.2108 7.03914 15.5858 7.41421C15.9609 7.78929 16.4696 8 17.0001 8C17.5305 8 18.0392 7.78929 18.4143 7.41421C18.7893 7.03914 19.0001 6.53043 19.0001 6C19.0001 5.46957 18.7893 4.96086 18.4143 4.58579C18.0392 4.21071 17.5305 4 17.0001 4V4ZM11.0001 7.76L7.10006 11.66C5.25006 13.5 4.31006 14.85 3.06006 18.16L4.94006 18.86C5.94006 16.2 6.66006 15.14 7.87006 13.84L9.22006 15.19L4.27006 20.14L5.69006 21.56L11.0001 16.24V7.76Z" />
</svg>
			</div><h2>{{sportname[10]}}</h2></span></li>
			<li><span class="flex gap-6 items-center cursor-pointer" @click="reset(sportname[11])"><div>
				<svg class="fill-black/10 hover:fill-blue-600" :class="{'fill-blue-600': tennis}" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M18.0001 15.0001C19.0609 15.0001 20.0783 15.4216 20.8285 16.1717C21.5786 16.9219 22.0001 17.9393 22.0001 19.0001C22.0001 20.061 21.5786 21.0784 20.8285 21.8286C20.0783 22.5787 19.0609 23.0001 18.0001 23.0001C16.9392 23.0001 15.9218 22.5787 15.1716 21.8286C14.4215 21.0784 14.0001 20.061 14.0001 19.0001C14.0001 17.9393 14.4215 16.9219 15.1716 16.1717C15.9218 15.4216 16.9392 15.0001 18.0001 15.0001ZM18.0001 17.0001C17.4696 17.0001 16.9609 17.2109 16.5858 17.5859C16.2108 17.961 16.0001 18.4697 16.0001 19.0001C16.0001 19.5306 16.2108 20.0393 16.5858 20.4144C16.9609 20.7894 17.4696 21.0001 18.0001 21.0001C18.5305 21.0001 19.0392 20.7894 19.4143 20.4144C19.7893 20.0393 20.0001 19.5306 20.0001 19.0001C20.0001 18.4697 19.7893 17.961 19.4143 17.5859C19.0392 17.2109 18.5305 17.0001 18.0001 17.0001ZM6.05006 14.5401C6.05006 14.5401 7.46006 13.1201 7.47006 10.3001C7.11006 8.11014 7.97006 5.54014 9.94006 3.58014C12.8701 0.650143 17.1401 0.170143 19.5001 2.50014C21.8301 4.86014 21.3501 9.13014 18.4201 12.0601C16.4601 14.0301 13.8901 14.8901 11.7001 14.5301C8.88006 14.5401 7.46006 15.9501 7.46006 15.9501L3.22006 20.1901L1.81006 18.7801L6.05006 14.5401ZM18.0701 3.93014C16.5001 2.37014 13.5001 2.84014 11.3501 5.00014C9.21006 7.14014 8.73006 10.1501 10.2901 11.7101C11.8601 13.2701 14.8601 12.7901 17.0001 10.6501C19.1601 8.50014 19.6301 5.50014 18.0701 3.93014Z" />
</svg>
			</div><h2>{{sportname[11]}}</h2></span></li>
			<hr>
			<li><a href="" class="flex gap-6 items-center cursor-pointer"><img src="./assets/stream.svg"><h2>Live Stream</h2></a></li>
		</ul>
	</nav>

	<div class="hidden lg:block fixed z-40 inset-0 w-screen h-screen bg-white/30 backdrop-blur-sm" v-if="expand" @click="expand = !expand"></div>

	<NavBar />
	<div class="flex flex-col lg:flex-row scores overflow-y-scroll">
		<CricketMatchHist class="hidden xl:block" :event="event" :link="link" v-if="cricket" />
		<TennisMatchHist class="hidden xl:block" :event="event" v-else-if="tennis || tt" />
		<div class="hidden xl:flex flex-col h-scores p-6 lg:p-8 border-r-2 border-slate-200" v-else>
			<section class="flex flex-col w-matches gap-6">
				<h1 class="font-bold">{{ event }} Matches</h1>
				<div class="grid gap-4 grid-cols-1 justify-items-center py-3 border-x-2 border-t-2 rounded-t-xl text-lg" style="background-color: #FFC758; border-color: #FFC758;">
					<div class="font-bold">Previous Matches</div>
				</div>
			</section>
			<div class="flex flex-col border-2 border-slate-200 bg-slate-100 rounded-b-xl divide-y-2 divide-dashed w-matches h-matches overflow-y-scroll">
				<section v-for="i in spSet" :key="i">
					<div class="grid gap-4 grid-cols-3 justify-items-center text-slate-600 py-2">
						<div class="font-bold">{{ i.team_1 }}</div>
						<section class="flex gap-2">
							<span>{{ i.running_score }}</span>
						</section>
						<div class="font-bold">{{ i.team_2 }}</div>
					</div>
				</section>
			</div>
		</div>

		<div class="flex flex-col gap-6 lg:gap-10 h-scores w-sc lg:w-full px-6 lg:px-12 py-6 bg-slate-200 border-r-2 border-slate-200 overflow-y-scroll">
			<div class="flex flex-col gap-3 lg:gap-6">
				<h1 class="font-bold text-slate-500">Recent</h1>
				<CricketScore :t1="spSet[0].bat_team" :t2="spSet[0].bowl_team" :score1="spSet[0].t1_score" :score2="spSet[0].t2_score" :overs="spSet[0].overs" :winner="spSet[0].winner" v-if="cricket" />
				<TennisScore :t1="spSet[0].team_1" :t2="spSet[0].team_2" :score="spSet[0].running_score" :set="spSet[0].set" v-else-if="tennis || tt" />
				<ScoreCard :t1="spSet[0].team_1" :t2="spSet[0].team_2" :score="spSet[0].running_score" v-else />
			</div>
			<div class="flex flex-col gap-3 lg:gap-6">
				<h1 class="font-bold text-slate-500">Last Match</h1>
				<CricketScore :t1="spSet[1].bat_team" :t2="spSet[1].bowl_team" :score1="spSet[1].t1_score" :score2="spSet[1].t2_score" :overs="spSet[1].overs" :winner="spSet[1].winner" v-if="cricket" />
				<TennisScore :t1="spSet[1].team_1" :t2="spSet[1].team_2" :score="spSet[1].running_score" :set="spSet[1].set" v-else-if="tennis || tt" />
				<ScoreCard :t1="spSet[1].team_1" :t2="spSet[1].team_2" :score="spSet[1].running_score" v-else />
			</div>
		</div>

		<div class="flex flex-col gap-6 h-scores p-6 lg:p-8 border-r-2 border-slate-200 bg-slate-50 xl:bg-white">
			<h1 class="font-bold">Standings</h1>
			<section class="overflow-y-scroll" v-for="v in set" :key="v">
				<div v-for="(vi, x) in v" :key="vi">
					<section class="flex flex-col gap-4 w-matches">
						<h1 class="font-bold">{{ x }}</h1>
						<div class="grid gap-4 grid-cols-3 px-4 py-3 border-x-2 border-t-2 rounded-t-xl text-lg" style="background-color: #FFC758; border-color: #FFC758;">
							<div v-for="(k, ind) in vi" :key="k" class="font-bold">{{ ind }}</div>
						</div>
					</section>
					<div class="mb-6 flex flex-col border-2 border-slate-200 bg-slate-100 rounded-b-xl divide-y-2 divide-dashed w-matches h-matches overflow-y-scroll">
						<section v-for="st in v" :key="st">
							<div class="grid gap-4 grid-cols-3 text-slate-600 px-4 py-2">
								<div v-for="i in st" :key="i">{{ i }}</div>
							</div>
						</section>
					</div>
				</div>
			</section>
		</div>

		<CricketMatchHist class="xl:hidden block" :event="event" v-if="cricket" />
		<TennisMatchHist class="xl:hidden block" :event="event" v-else-if="tennis || tt" />
		<div class="xl:hidden flex flex-col h-scores p-6 lg:p-8 border-r-2 border-slate-200 bg-slate-50 xl:bg-white" v-else>
			<section class="flex flex-col w-matches gap-6">
				<h1 class="font-bold">{{ event }} Matches</h1>
				<div class="grid gap-4 grid-cols-1 justify-items-center py-3 border-x-2 border-t-2 rounded-t-xl text-lg" style="background-color: #FFC758; border-color: #FFC758;">
					<div class="font-bold">Previous Matches</div>
				</div>
			</section>
			<div class="flex flex-col border-2 border-slate-200 bg-slate-100 rounded-b-xl divide-y-2 divide-dashed w-matches h-matches overflow-y-scroll">
				<section v-for="i in spSet" :key="i">
					<div class="grid gap-4 grid-cols-3 justify-items-center text-slate-600 py-2">
						<div class="font-bold">{{ i.team_1 }}</div>
						<section class="flex gap-2">
							<span>{{ i.running_score }}</span>
						</section>
						<div class="font-bold">{{ i.team_2 }}</div>
					</div>
				</section>
			</div>
		</div>
	</div>
</template>

<script>
import axios from 'axios';
export default {
	data() {
		return {
			expand: false,
			event: "Cricket",
			link: "https://cricheroes.in/tournament/424723/AIRO-2K22",
			set: [],
			spSet: [],
			sportname: [
				"Cricket",
				"Basketball",
				"Badminton",
				"Football",
				"Volleyball",
				"Throwball",
				"Chess",
				"TT",
				"Pool",
				"Snooker",
				"KhoKho",
				"Tennis"
			],
			cricket: true,
			basketball: false,
			badminton: false,
			football: false,
			volleyball: false,
			throwball: false,
			chess: false,
			tt: false,
			pool: false,
			snooker: false,
			kho: false,
			tennis: false
		}
	},
	created() {
		axios
			.get("https://raw.githubusercontent.com/Airo-MU/matches/master/cricket/cricket.json")
			.then((res) => {
				this.spSet = res.data
			})
		axios
			.get("https://raw.githubusercontent.com/Airo-MU/matches/master/cricket/test.json")
			.then((res) => {
				this.set = res.data
			})
	},
	methods: {
		callJSON(sp) {
			axios
			.get(`https://raw.githubusercontent.com/Airo-MU/matches/master/${sp}/${sp}.json`)
			.then((res) => {
				this.spSet = res.data
			})
			axios
			.get(`https://raw.githubusercontent.com/Airo-MU/matches/master/${sp}/standings.json`)
			.then((res) => {
				this.set = res.data
			})
		},
		reset(item) {
			this.expand = false
			this.cricket = false
			this.basketball = false
			this.badminton = false
			this.football = false
			this.volleyball = false
			this.throwball = false
			this.chess = false
			this.tt = false
			this.pool = false
			this.snooker = false
			this.kho = false
			this.tennis = false

			var inx = this.sportname.indexOf(item)
			switch (inx) {
				case 0:
					this.cricket = true;
					this.callJSON("cricket")
					this.event = this.sportname[0]
					break;
				case 1:
					this.basketball = true;
					this.callJSON("basketball")
					this.event = this.sportname[1]
					break;
				case 2:
					this.badminton = true;
					this.callJSON("badminton")
					this.event = this.sportname[2]
					break;
				case 3:
					this.football = true;
					this.callJSON("football")
					this.event = this.sportname[3]
					break;
				case 4:
					this.volleyball = true;
					this.callJSON("volleyball")
					this.event = this.sportname[4]
					break;
				case 5:
					this.throwball = true;
					this.callJSON("throwball")
					this.event = this.sportname[5]
					break;
				case 6:
					this.chess = true;
					this.callJSON("chess")
					this.event = this.sportname[6]
					break;
				case 7:
					this.tt = true;
					this.callJSON("tt")
					this.event = this.sportname[7]
					break;
				case 8:
					this.pool = true;
					this.callJSON("pool")
					this.event = this.sportname[8]
					break;
				case 9:
					this.snooker = true;
					this.callJSON("snooker")
					this.event = this.sportname[9]
					break;
				case 10:
					this.kho = true;
					this.callJSON("kho")
					this.event = this.sportname[10]
					break;
				case 11:
					this.tennis = true;
					this.callJSON("tennis")
					this.event = this.sportname[11]
					break;
				default:
					break;
			}
		}
	},
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

::-webkit-scrollbar {
	width: 0px;
	background: transparent;
}

#app {
	font-family: 'Montserrat', sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: black;
	display: flex;
	flex-direction: column;
}

.scores {
	max-width: calc(100vw - 62px);
	margin-left: 62px;
}

.h-scores {
	height: calc(100vh - 78.04px);
}

.w-side {
	width: 260px;
}

.standings {
	min-width: 360px;
}

.w-matches {
	width: 320px;
}

.h-matches {
	max-height: 506px;
}

@media (max-width: 1024px) {
	.scores {
		width: calc(100vw - 62px);
	}

	.h-scores {
		height: auto;
	}

	.w-sc {
		max-width: calc(100vw - 62px);
	}

	.w-matches {
		width: auto;
	}
}
</style>
