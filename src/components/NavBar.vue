<template>
	<div>
		<nav
			class="relative flex flex-wrap items-center justify-between px-2 py-3 bg-black mb-3 pt-5"
		>
			<div
				class="container px-4 mx-auto flex flex-wrap items-center justify-between"
			>
				<div
					class="w-full relative flex justify-between lg:w-auto px-4 lg:static lg:block lg:justify-start"
				>
					<a
						class="text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap uppercase text-white"
						href="#pablo"
					>
						<svg
							width="86"
							height="25"
							viewBox="0 0 86 25"
							fill="none"
							xmlns="http://www.w3.org/2000/svg"
						>
							<path
								d="M29.4541 24.6787V1.28535H37.4842C40.1341 1.28535 42.1511 1.81555 43.535 2.87596C44.919 3.93638 45.6109 5.51628 45.6109 7.61568C45.6109 8.6868 45.3213 9.65081 44.7419 10.5077C44.1626 11.3646 43.3151 12.0287 42.1993 12.5C43.4653 12.8428 44.4416 13.4908 45.1282 14.4441C45.8255 15.3867 46.1742 16.5221 46.1742 17.8503C46.1742 20.0461 45.4661 21.7331 44.05 22.9113C42.6446 24.0895 40.6276 24.6787 37.9992 24.6787H29.4541ZM33.5255 14.1228V21.4332H38.0475C39.3241 21.4332 40.3219 21.1172 41.0407 20.4852C41.7595 19.8533 42.1189 18.9749 42.1189 17.8503C42.1189 15.4188 40.8744 14.1763 38.3854 14.1228H33.5255ZM33.5255 11.1343H37.5164C38.7824 11.1343 39.7694 10.8505 40.4774 10.2828C41.1962 9.70437 41.5556 8.89032 41.5556 7.84062C41.5556 6.6838 41.2231 5.84833 40.5579 5.33419C39.9035 4.82005 38.8789 4.56298 37.4842 4.56298H33.5255V11.1343Z"
								fill="white"
							/>
							<path
								d="M49.1352 15.8258C49.1352 14.1228 49.4731 12.591 50.149 11.2307C50.8249 9.85968 51.7744 8.80998 52.9974 8.08162C54.2204 7.34255 55.6258 6.97301 57.2136 6.97301C59.5631 6.97301 61.4674 7.72815 62.9264 9.23843C64.3962 10.7487 65.1901 12.7517 65.3081 15.2474L65.3242 16.1632C65.3242 17.877 64.9916 19.4087 64.3265 20.7584C63.6721 22.108 62.728 23.1523 61.4942 23.8914C60.2712 24.6305 58.855 25 57.2458 25C54.789 25 52.8204 24.1859 51.3399 22.5578C49.8701 20.919 49.1352 18.7393 49.1352 16.0186V15.8258ZM53.0457 16.1632C53.0457 17.952 53.4158 19.3552 54.156 20.3728C54.8963 21.3796 55.9262 21.883 57.2458 21.883C58.5654 21.883 59.5899 21.3689 60.3195 20.3406C61.0597 19.3123 61.4298 17.8074 61.4298 15.8258C61.4298 14.0692 61.049 12.6767 60.2873 11.6485C59.5363 10.6202 58.5117 10.106 57.2136 10.106C55.9369 10.106 54.9231 10.6148 54.1721 11.6324C53.4211 12.6392 53.0457 14.1495 53.0457 16.1632Z"
								fill="white"
							/>
							<path
								d="M72.7911 24.6787H68.8806V0H72.7911V24.6787Z"
								fill="white"
							/>
							<path
								d="M81.9638 3.06877V7.29434H85.0375V10.1864H81.9638V19.8907C81.9638 20.5548 82.0926 21.0368 82.35 21.3368C82.6182 21.626 83.0903 21.7706 83.7662 21.7706C84.2168 21.7706 84.6727 21.717 85.134 21.6099V24.6305C84.2436 24.8768 83.3853 25 82.5592 25C79.5553 25 78.0534 23.3451 78.0534 20.0353V10.1864H75.1889V7.29434H78.0534V3.06877H81.9638Z"
								fill="white"
							/>
							<path
								d="M0 16.0117H14.7131V24.8255L23.541 10.1358H8.82787V1.32202L0 16.0117Z"
								fill="#006CFF"
							/>
						</svg>
					</a>
					<button
						class="text-white cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
						type="button"
						v-on:click="toggleNavbar()"
					>
						<i class="fa fa-bars" aria-hidden="true"></i>
					</button>
				</div>
				<div
					v-bind:class="{ hidden: !showMenu, flex: showMenu }"
					class="lg:flex lg:flex-grow items-center"
				>
					<ul class="flex flex-col lg:flex-row list-none ml-8">
						<li class="nav-item">
							<a
								class="px-3 py-2 flex items-center text-base capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2">CheckoutOS</span>
							</a> </li
						><li class="nav-item">
							<a
								class="px-3 py-2 flex items-center text-base capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2">Learn</span>
							</a> </li
						><li class="nav-item">
							<a
								class="px-3 py-2 flex text-base capitalize items-center font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2">Developers</span>
							</a> </li
						><li class="nav-item">
							<a
								class="px-3 py-2 flex text-base items-center capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2">Remote Checkout</span>
							</a>
						</li>
						<li class="nav-item">
							<a
								class="px-3 py-3 flex items-center text-xs capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2 text-xs">Login </span>
							</a>
						</li>
						<li class="nav-item">
							<a
								class="px-3 py-3 flex items-center text-xs capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2 text-xs">Contact Sales </span>
							</a>
						</li>
					</ul>
					<div class="relative flex flex-wrap items-stretch pl-10 w-60">
						<input
							type="email"
							placeholder="Get Bolt Updates"
							class="px-3 py-3 placeholder-slate-400 text-blueGray-600 relative bg-white rounded text-sm border-0 shadow outline-none focus:outline-none w-full focus:ring pr-10"
						/>
						<span
							class="-z-0 leading-snug font-normal text-center absolute text-blue-500 bg-transparent rounded text-base items-center justify-center w-8 right-0 pr-3 py-3 cursor-pointer"
						>
							<i class="fa fa-envelope-o" aria-hidden="true"></i>
						</span>
					</div>
					<div
						class="hover:text-white text-slate-300 text-2xl pl-10 cursor-pointer ease-linear transition-all duration-150"
						v-on:click="toggleModal()"
					>
						<i class="fa fa-search" aria-hidden="true"></i>
					</div>
					<div v-if="showModal" class="fixed inset-0 z-50 flex">
						<div class="relative w-full">
							<!--modal-->
							<div
								class="border-0 shadow-lg relative flex flex-col w-full bg-white outline-none focus:outline-none"
							>
								<div
									class="flex items-start justify-between p-5 border-b border-solid border-blueGray-200 rounded-t"
								>
									<div class="flex flex-row">
										<h3 class="text-3xl font-semibold">
											<i class="fa fa-search" aria-hidden="true"></i>
										</h3>
										<input
											type="search"
											placeholder="SEARCH"
											class="placeholder-slate-800 text-blueGray-600 relative bg-white text-sm border-0 outline-none focus:outline-none w-40 focus:ring-0 ml-4"
										/>
									</div>
									<button
										class="border-0 text-black float-right text-4xl leading-none opacity-80"
										v-on:click="toggleModal()"
									>
										<span
											class="text-black opacity-60 h-6 w-6 text-4xl block outline-none focus:outline-none"
										>
											×
										</span>
									</button>
								</div>
							</div>
						</div>
					</div>
					<div v-if="showModal" class="opacity-25 fixed inset-0 z-40 bg-black">
					</div>
				</div>
			</div>
		</nav>
	</div>
</template>

<style scoped></style>
<script>
export default {
	name: 'pink-navbar',
	name: 'large-modal',
	data() {
		return {
			showMenu: false,
			showModal: false,
		};
	},
	methods: {
		toggleNavbar: function () {
			this.showMenu = !this.showMenu;
		},
		toggleModal: function () {
			this.showModal = !this.showModal;
		},
	},
};
</script>
