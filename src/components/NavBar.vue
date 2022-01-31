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
						<li class="nav-item" @mouseover="showDropDown()">
							<a
								class="px-3 py-2 flex items-center text-base capitalize font-bold leading-snug hover:text-white text-slate-300"
								href="#"
							>
								<span class="ml-2">CheckoutOS</span>
							</a>
						</li>
						<div
							v-show="navDropDown"
							class="py-2 mt-12 bg-slate-50 rounded-md shadow-xl lg:absolute lg:left-14 w-8/12 z-40"
						>
							<!-- dropdown -->
							<div class="">
								<div class="flex flex-row">
									<div class="col1 w-3/4">
										<div class="row1">
											<a href="" class="flex flex-row mx-30 py-5 w-full">
												<div class="text-center">
													<h6
														class="text-xl leading-5 text-gray-800 font-bold mb-8 transition"
														>Bolt CheckoutOS</h6
													>
													<p
														class="text-sm leading-2 text-gray-800 font-medium transition"
														>CheckoutOS powers one-click checkout, payments
														orchestration, shopper identity &amp; accounts, and
														post-purchase experiences</p
													>
												</div>
												<div class="w-2/5">
													<div
														class="flex self-start rounded-sm mt-10 pt-3 pb-3 pl-3 pr-3 text-white text-sm tracking-normal duration-200 font-medium bg-blue-500 transition"
													>
														<svg
															class="relative"
															width="18"
															height="18"
															viewBox="0 0 18 18"
															fill="none"
															xmlns="http://www.w3.org/2000/svg"
														>
															<path
																d="M0.299316 11.2552H10.9419V17.6204L17.326 7.01169H6.68336V0.646454L0.299316 11.2552Z"
																fill="white"
															></path>
														</svg>
														<span>Learn More</span>
													</div>
												</div>
											</a>
										</div>
										<div class="row2 grid grid-cols-2">
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-2 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-4">
															<svg
																class="platform-menu-graphic"
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	id="Union"
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M26.1449 12.3639H16.7511L22.386 3V8.61831H31.7798L26.1449 17.9822V12.3639ZM2.62991 5.88994C2.09271 5.88994 1.65723 6.32542 1.65723 6.86262C1.65723 7.39982 2.09271 7.83531 2.62991 7.83531H4.73772C5.83275 7.83531 6.38702 8.01452 6.70285 8.24939C6.99354 8.46557 7.24133 8.84895 7.41376 9.68261L7.71723 11.4407L7.72152 11.4639L10.1726 23.8626C10.1761 23.8802 10.18 23.8977 10.1845 23.9152L11.0268 27.2057L11.0304 27.2194C11.2642 28.0798 11.5597 28.9932 12.205 29.6607C12.9049 30.3847 13.8622 30.6792 15.0822 30.6792H33.7606C34.2978 30.6792 34.7333 30.2437 34.7333 29.7065C34.7333 29.1693 34.2978 28.7338 33.7606 28.7338H15.0822C14.1749 28.7338 13.8107 28.5228 13.6036 28.3085C13.3424 28.0383 13.1453 27.5824 12.9096 26.7162L12.3798 24.6466H34.8307C35.2609 24.6466 35.6399 24.3641 35.7628 23.9519L39.4596 11.5531C39.5474 11.2588 39.4909 10.9402 39.3074 10.6939C39.1238 10.4476 38.8347 10.3025 38.5275 10.3025H34.1821L34.158 10.3028V10.3008H33.5325L32.3376 12.2461H34.1229C34.1425 12.2473 34.1622 12.2479 34.1821 12.2479H37.2225L34.1057 22.7013H11.926L9.85954 12.2479H13.5256C13.5614 12.2479 13.5967 12.246 13.6314 12.2422H14.088L15.2828 10.3047H13.5915C13.5697 10.3033 13.5478 10.3025 13.5256 10.3025H9.49491L9.32814 9.33642C9.32644 9.32657 9.32459 9.31674 9.32259 9.30694C9.106 8.24814 8.70639 7.31501 7.86375 6.68837C7.04461 6.07919 5.97749 5.88994 4.73772 5.88994H2.62991ZM16.6335 33.9427C15.9692 33.9427 15.4306 34.4812 15.4306 35.1456C15.4306 35.81 15.9692 36.3485 16.6335 36.3485C17.2979 36.3485 17.8365 35.81 17.8365 35.1456C17.8365 34.4812 17.2979 33.9427 16.6335 33.9427ZM13.4852 35.1456C13.4852 33.4068 14.8948 31.9973 16.6335 31.9973C18.3723 31.9973 19.7818 33.4068 19.7818 35.1456C19.7818 36.8843 18.3723 38.2939 16.6335 38.2939C14.8948 38.2939 13.4852 36.8843 13.4852 35.1456ZM28.6638 35.1456C28.6638 34.4927 29.1931 33.9635 29.8459 33.9635C30.4988 33.9635 31.0281 34.4927 31.0281 35.1456C31.0281 35.7985 30.4988 36.3277 29.8459 36.3277C29.1931 36.3277 28.6638 35.7985 28.6638 35.1456ZM29.8459 32.0181C28.1187 32.0181 26.7185 33.4183 26.7185 35.1456C26.7185 36.8729 28.1187 38.2731 29.8459 38.2731C31.5732 38.2731 32.9734 36.8729 32.9734 35.1456C32.9734 33.4183 31.5732 32.0181 29.8459 32.0181Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<clipPath id="clip0">
																		<rect
																			width="52"
																			height="52"
																			fill="white"
																		></rect>
																	</clipPath>
																	<linearGradient
																		id="paint0_linear"
																		x1="1"
																		y1="2"
																		x2="17.6833"
																		y2="46.5979"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p class="w-full text-sm font-bold pb-5"
																>Checkout</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Lightning quick checkout to turn shoppers into
																paying customers</small
															>
														</div>
													</span>
												</a>
											</div>
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-4 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
													style="
														border-right: 1px solid #eeeeee;
														border-bottom: 1px solid #eeeeee;
													"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-2">
															<svg
																class="platform-menu-graphic"
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	id="Union"
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M34.7967 10.6056H27.1904L31.7531 3V7.56334H39.3593L34.7967 15.1689V10.6056ZM4.56223 22.913C4.56223 14.4148 11.4514 7.52561 19.9496 7.52561C21.5909 7.52561 23.1706 7.78228 24.6515 8.257C25.1276 8.4096 25.6372 8.14739 25.7898 7.67136C25.9424 7.19532 25.6802 6.68572 25.2041 6.53313C23.5467 6.00184 21.7807 5.71533 19.9496 5.71533C10.4516 5.71533 2.75195 13.415 2.75195 22.913C2.75195 32.4109 10.4516 40.1106 19.9496 40.1106C29.4476 40.1106 37.1472 32.4109 37.1472 22.913C37.1472 21.0818 36.8607 19.3158 36.3294 17.6584C36.1768 17.1824 35.6672 16.9202 35.1912 17.0728C34.7151 17.2254 34.4529 17.735 34.6055 18.211C35.0803 19.692 35.3369 21.2716 35.3369 22.913C35.3369 31.4112 28.4478 38.3003 19.9496 38.3003C11.4514 38.3003 4.56223 31.4112 4.56223 22.913ZM19.9494 12.9565C14.4506 12.9565 9.99289 17.4142 9.99289 22.913C9.99289 25.1247 10.714 27.1679 11.934 28.8205C12.0498 28.4639 12.1953 28.1238 12.3572 27.8C12.9363 26.7384 14.4468 26.2356 16.709 25.4827C16.7907 25.4555 16.8735 25.4279 16.9572 25.4L17.3572 25.3V24.7C16.4572 23.8 15.9572 22.8 15.9572 20.8C15.9572 18.6 17.5572 17 19.7572 17C21.9572 17 23.6572 18.6 23.6572 20.8C23.6572 22.8 23.0572 23.8 22.2572 24.6C22.2572 24.6667 22.2461 24.7444 22.235 24.8222C22.2128 24.9778 22.1906 25.1333 22.2572 25.2L22.6572 25.4C22.741 25.4279 22.8237 25.4555 22.9055 25.4827C25.1677 26.2356 26.6782 26.7384 27.2572 27.8C27.4925 28.2235 27.6613 28.647 27.7742 29.0704C29.1093 27.3761 29.9059 25.2376 29.9059 22.913C29.9059 17.4142 25.4482 12.9565 19.9494 12.9565ZM26.162 30.694C26.1588 30.6631 26.1572 30.6318 26.1572 30.6C26.1572 29.9 25.9572 29.3 25.6572 28.7C25.4891 28.3637 24.119 27.8859 22.8548 27.4451C22.6155 27.3617 22.38 27.2796 22.1572 27.2L21.4572 26.9C21.2572 26.8 20.6572 26.5 20.4572 25.7C20.3572 25.1 20.3572 24 20.8572 23.4C21.3572 22.9 21.7572 22.3 21.7572 20.7C21.7572 18.9 20.1572 18.7 19.7572 18.7C19.3572 18.7 17.7572 18.8 17.7572 20.7C17.7572 22.3 18.1572 22.8 18.6572 23.4C19.2572 24 19.2572 25.1 19.1572 25.7C18.9572 26.5 18.4572 26.8 18.1572 26.9L17.5572 27.1C16.0572 27.6 14.2572 28.2 14.0572 28.6C13.7572 29.2 13.5572 29.9 13.5572 30.5C13.5572 30.5154 13.5568 30.5306 13.5558 30.5458C15.2855 31.9962 17.5155 32.8696 19.9494 32.8696C22.2993 32.8696 24.459 32.0555 26.162 30.694ZM8.18262 22.913C8.18262 16.4144 13.4508 11.1462 19.9494 11.1462C26.448 11.1462 31.7162 16.4144 31.7162 22.913C31.7162 29.4117 26.448 34.6798 19.9494 34.6798C13.4508 34.6798 8.18262 29.4117 8.18262 22.913Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<clipPath id="clip0">
																		<rect
																			width="52"
																			height="52"
																			fill="white"
																		></rect>
																	</clipPath>
																	<linearGradient
																		id="paint0_linear"
																		x1="10"
																		y1="8"
																		x2="29.7865"
																		y2="50.6642"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p
																class="small-border-top w-full text-sm font-bold platform-text pb-1"
																>Identity &amp; Accounts</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Give shoppers a secure one-click checkout
																anywhere across the network</small
															>
														</div>
													</span>
												</a>
											</div>
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-2 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
													style="
														border-right: 1px solid #eeeeee;
														border-bottom: 1px solid #eeeeee;
													"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-10">
															<svg
																class="platform-menu-graphic"
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	id="Union"
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M8.4675 9.82389C8.4675 9.29446 8.79377 8.73678 9.66625 8.16262C10.5316 7.59314 11.7746 7.12259 13.2024 6.75594C16.049 6.02499 19.3596 5.77364 21.1184 5.81445C21.1324 5.81478 21.1464 5.81478 21.1604 5.81445C22.9193 5.77364 26.2299 6.02499 29.0765 6.75594C30.5043 7.12259 31.7472 7.59314 32.6126 8.16262C33.4851 8.73678 33.8114 9.29446 33.8114 9.82389V11.7266C28.976 10.2577 25.0346 9.50542 21.083 9.50506C17.1358 9.50471 13.2312 10.2545 8.4675 11.7213V9.82389ZM21.0828 11.3153C24.9291 11.3157 28.8212 12.0716 33.8114 13.6203V21.5319C33.4409 25.2668 30.3942 33.2661 21.1394 35.6516C11.8847 33.2661 8.83798 25.2668 8.4675 21.5318V13.6174C13.3837 12.0693 17.2388 11.315 21.0828 11.3153ZM12.7522 5.00255C15.7672 4.22834 19.2308 3.96243 21.1394 4.00419C23.048 3.96243 26.5116 4.22834 29.5267 5.00255C31.0353 5.38991 32.4998 5.92128 33.6078 6.65041C34.7087 7.37487 35.6217 8.41251 35.6217 9.82389V12.9559V21.5756C35.6217 21.6041 35.6203 21.6325 35.6176 21.6609C35.2179 25.8826 31.8102 34.8946 21.3554 37.4639C21.2136 37.4988 21.0653 37.4988 20.9234 37.4639C10.4686 34.8946 7.06094 25.8826 6.66126 21.6609C6.65857 21.6325 6.65723 21.6041 6.65723 21.5756V12.9559V9.82389C6.65723 8.41251 7.57022 7.37487 8.6711 6.65041C9.77908 5.92128 11.2436 5.38991 12.7522 5.00255ZM22.4097 23.5031H14.8035L19.3661 15.8976V20.4609H26.9724L22.4097 28.0665V23.5031Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<clipPath id="clip0">
																		<rect
																			width="52"
																			height="52"
																			fill="white"
																		></rect>
																	</clipPath>
																	<linearGradient
																		id="paint0_linear"
																		x1="5"
																		y1="3"
																		x2="24.7865"
																		y2="45.6642"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p
																class="small-border-top w-full text-sm font-bold platform-text pb-1"
																>Fraud Protection</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Stay protected against fraud while approving
																more good orders</small
															>
														</div>
													</span>
												</a>
											</div>
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-2 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
													style="
														border-right: 1px solid #eeeeee;
														border-bottom: 1px solid #eeeeee;
													"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-10">
															<svg
																class="platform-menu-graphic"
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	id="Union"
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M6.75677 7.78955C4.20529 7.78955 2.1369 9.85794 2.1369 12.4094V28.579C2.1369 31.1305 4.20529 33.1988 6.75677 33.1988H24.8898C25.4001 33.1988 25.8137 32.7852 25.8137 32.2749C25.8137 31.7646 25.4001 31.3509 24.8898 31.3509H6.75677C5.22588 31.3509 3.98485 30.1099 3.98485 28.579V15.73H33.6098V19.004C33.6098 19.5143 34.0234 19.928 34.5337 19.928C35.044 19.928 35.4577 19.5143 35.4577 19.004V12.4094C35.4577 9.85794 33.3893 7.78955 30.8378 7.78955H6.75677ZM33.6098 13.882H3.98485V12.4094C3.98485 10.8785 5.22588 9.6375 6.75677 9.6375H30.8378C32.3687 9.6375 33.6098 10.8785 33.6098 12.4094V13.882ZM33.9644 28.3293H24.131L30.0297 18.5271V24.4084H39.8631L33.9644 34.2106V28.3293ZM7.27652 21.2738C7.27652 20.7635 7.6902 20.3498 8.2005 20.3498H21.0206C21.5309 20.3498 21.9446 20.7635 21.9446 21.2738C21.9446 21.7841 21.5309 22.1978 21.0206 22.1978H8.2005C7.6902 22.1978 7.27652 21.7841 7.27652 21.2738ZM8.2005 25.0275C7.6902 25.0275 7.27652 25.4411 7.27652 25.9514C7.27652 26.4617 7.6902 26.8754 8.2005 26.8754H13.0514C13.5617 26.8754 13.9753 26.4617 13.9753 25.9514C13.9753 25.4411 13.5617 25.0275 13.0514 25.0275H8.2005Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<clipPath id="clip0">
																		<rect
																			width="52"
																			height="52"
																			fill="white"
																		></rect>
																	</clipPath>
																	<linearGradient
																		id="paint0_linear"
																		x1="26.4063"
																		y1="22"
																		x2="32.9146"
																		y2="38.2262"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p
																class="small-border-top w-full text-sm font-bold platform-text pb-1"
																>Payments Orchestration</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Payment processing integrations and solutions
																that scale</small
															>
														</div>
													</span>
												</a>
											</div>
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-2 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
													style="
														border-right: 1px solid #eeeeee;
														border-bottom: 1px solid #eeeeee;
													"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-10">
															<svg
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M10.3478 11.6505H19.1808V15.5406C19.1808 16.122 19.6521 16.5933 20.2334 16.5933C20.8148 16.5933 21.2861 16.122 21.2861 15.5406V11.6505H32.3616V15.5406C32.3616 16.122 32.8329 16.5933 33.4142 16.5933C33.9956 16.5933 34.4669 16.122 34.4669 15.5406V11.6505H37.4326C37.9032 13.5431 39.6139 14.9457 41.6522 14.9457C44.0534 14.9457 46 12.9991 46 10.5979C46 8.19665 44.0534 6.25006 41.6522 6.25006C39.6139 6.25006 37.9033 7.6526 37.4327 9.54523H33.4142H20.2334H10.3478C7.94659 9.54523 6 11.4918 6 13.8931V28.7214C6 29.3028 6.47128 29.774 7.05263 29.774C7.63398 29.774 8.10526 29.3028 8.10526 28.7214V13.8931C8.10526 12.6545 9.10929 11.6505 10.3478 11.6505ZM41.6522 12.8404C40.4137 12.8404 39.4096 11.8364 39.4096 10.5979C39.4096 9.35933 40.4137 8.35532 41.6522 8.35532C42.8907 8.35532 43.8947 9.35935 43.8947 10.5979C43.8947 11.8364 42.8907 12.8404 41.6522 12.8404ZM15.7482 19.4309C14.0042 19.4309 12.5903 20.8447 12.5903 22.5888V43.0922C12.5903 44.8362 14.0042 46.2501 15.7482 46.2501H37.8992C39.6433 46.2501 41.0571 44.8362 41.0571 43.0922V22.5888C41.0571 20.8447 39.6433 19.4309 37.8992 19.4309H34.4669V18.8359C34.4669 18.2546 33.9956 17.7833 33.4142 17.7833C32.8329 17.7833 32.3616 18.2546 32.3616 18.8359V19.4309H21.2861V18.8359C21.2861 18.2546 20.8148 17.7833 20.2334 17.7833C19.6521 17.7833 19.1808 18.2546 19.1808 18.8359V19.4309H15.7482ZM33.4093 21.5361H20.2384L20.2334 21.5361L20.2285 21.5361H15.7482C15.1669 21.5361 14.6956 22.0074 14.6956 22.5888V43.0922C14.6956 43.6735 15.1669 44.1448 15.7482 44.1448H37.8992C38.4806 44.1448 38.9519 43.6735 38.9519 43.0922V22.5888C38.9519 22.0074 38.4806 21.5361 37.8992 21.5361H33.4192L33.4142 21.5361L33.4093 21.5361ZM28.5562 34.5363H20.1528L25.1937 26.1336V31.1752H33.5971L28.5562 39.5779V34.5363Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<linearGradient
																		id="paint0_linear"
																		x1="6"
																		y1="6.25006"
																		x2="31.0726"
																		y2="54.0758"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p
																class="small-border-top w-full text-sm font-bold platform-text pb-1"
																>Analytics &amp; Insights</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Gain insights into buying behavior with
																reporting and data visualizations</small
															>
														</div>
													</span>
												</a>
											</div>
											<div>
												<a
													href=""
													class="relative dropdown-link flex items-start px-2 py-2 text-black justify-center text-center text-sm font-normal bg-white w-full border-t border-r"
													style="
														border-right: 1px solid #eeeeee;
														border-bottom: 1px solid #eeeeee;
													"
												>
													<span
														class="flex flex-row align-center justify-center items-center"
													>
														<div class="h-p52 w-p52 mb-10">
															<svg
																width="52"
																height="52"
																viewBox="0 0 52 52"
																fill="none"
																xmlns="http://www.w3.org/2000/svg"
															>
																<path
																	fill-rule="evenodd"
																	clip-rule="evenodd"
																	d="M9.96436 8.2276C8.85979 8.2276 7.96436 9.12303 7.96436 10.2276V22.5996C7.96436 23.7042 8.85979 24.5996 9.96436 24.5996H22.3364C23.4409 24.5996 24.3364 23.7042 24.3364 22.5996V10.2276C24.3364 9.12303 23.4409 8.2276 22.3364 8.2276H9.96436ZM9.96436 10.2276L22.3364 10.2276V22.5996H9.96436V10.2276ZM29.3364 8.2276C28.2319 8.2276 27.3364 9.12303 27.3364 10.2276V22.5996C27.3364 23.7042 28.2319 24.5996 29.3364 24.5996H41.7084C42.813 24.5996 43.7084 23.7042 43.7084 22.5996V10.2276C43.7084 9.12303 42.813 8.2276 41.7084 8.2276H29.3364ZM29.3364 10.2276L41.7084 10.2276V22.5996H29.3364V10.2276ZM7.96436 29.5995C7.96436 28.495 8.85979 27.5995 9.96436 27.5995H22.3364C23.4409 27.5995 24.3364 28.495 24.3364 29.5995V41.9715C24.3364 43.0761 23.4409 43.9715 22.3364 43.9715H9.96436C8.85979 43.9715 7.96436 43.0761 7.96436 41.9715V29.5995ZM22.3364 29.5995H9.96436V41.9715H22.3364V29.5995ZM37.2033 37.4655H28.8025L33.8418 29.0655V34.1055H42.2425L37.2033 42.5055V37.4655Z"
																	fill="url(#paint0_linear)"
																></path>
																<defs>
																	<linearGradient
																		id="paint0_linear"
																		x1="7.96436"
																		y1="8.2276"
																		x2="30.3691"
																		y2="50.9646"
																		gradientUnits="userSpaceOnUse"
																	>
																		<stop stop-color="#133EE3"></stop>
																		<stop
																			offset="1"
																			stop-color="#7532E1"
																		></stop>
																	</linearGradient>
																</defs>
															</svg>
														</div>
														<div class="flex flex-col text-left ml-2">
															<p
																class="small-border-top w-full text-sm font-bold platform-text pb-1"
																>View All Features</p
															>
															<small
																class="transition mt-1 text-xs font-medium pt-1"
																>Check out the full list of features that power
																Bolt's products</small
															>
														</div>
													</span>
												</a>
											</div>
										</div>
										<div class="row3 flex flex-row justify-center">
											<div class="py-2 px-1">
												<a
													href=""
													class="text-xs leading-3 font-bold text-gray-900 hover:text-blue transition-colors"
													>Services and Support</a
												>
												<span
													class="text-gray-900 text-xs leading-3"
													style="display: inline-block; margin: 0 15px"
													>|</span
												>
												<a
													href=""
													class="text-xs leading-3 font-bold text-gray-900 hover:text-blue transition-colors"
													>FAQs</a
												>
												<span
													class="text-gray-900 text-xs leading-16"
													style="display: inline-block; margin: 0 15px"
													>|</span
												>
												<a
													href=""
													class="text-xs leading-16 font-bold text-gray-900 hover:text-blue transition-colors"
													>Case Studies</a
												>
												<span
													class="text-grey-9 text-pxs leading-16"
													style="display: inline-block; margin: 0 15px"
													>|</span
												>
												<a
													href="/platform#hiwVideoTrigger"
													class="text-xs leading-16 font-bold text-grey-9 hover:text-blue transition-colors"
													>Overview Video</a
												>
												<span
													class="text-gray-900 text-sm leading-3"
													style="display: inline-block; margin: 0 15px"
													>|</span
												>
												<a
													href="/checkout-demo"
													class="text-xs leading-2 font-bold text-gray-900 hover:text-blue transition-colors"
													>Checkout Demo</a
												>
											</div>
										</div>
									</div>
									<div class="col2 w-1/4 ml-3 -my-2">
										<div style="">
											<div class=" " style="">
												<a
													href=""
													class="block relative py-2 px-5 mt-5 platform-rail-link"
												>
													<svg
														class="absolute opacity-25 platform-icon"
														style="top: 30px; right: 22px"
														width="27"
														height="43"
														viewBox="0 0 27 43"
														fill="none"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															d="M9.71868 25.2812C7.4707 25.2812 5.64835 27.1525 5.64835 29.4609C5.64835 33.4888 9.19279 37.1535 9.71868 39.1172C10.2446 41.0809 10.3806 42 10.3806 42H23.2864L25.4776 34.1255C25.8238 32.8803 25.9996 31.5918 26 30.2969V25.9778C26 24.8236 25.0888 23.888 23.9648 23.888H21.9297C21.9297 23.1185 21.3222 22.4948 20.5729 22.4948H17.8593C17.8593 21.7253 17.2519 21.1015 16.5026 21.1015H13.789V13.4387C13.789 12.2846 12.8778 11.3489 11.7538 11.3489C10.6299 11.3489 9.71868 12.2846 9.71868 13.4387V30.8541M17.8593 22.492V25.2785M13.789 21.0988V25.2785M21.9297 23.8853V26.6717M16.6509 15.4886C17.3063 14.5084 17.6897 13.3216 17.6897 12.0428C17.6897 8.6764 15.0322 5.9474 11.7538 5.9474C8.47554 5.9474 5.81795 8.6764 5.81795 12.0428C5.81795 13.6469 6.42137 15.1063 7.40784 16.1946M20.2023 18.8757C21.6461 16.996 22.5077 14.6227 22.5077 12.0428C22.5077 5.94403 17.693 1 11.7538 1C5.81466 1 1 5.94403 1 12.0428C1 15.9868 3.01358 19.448 6.04269 21.4013"
															stroke="white"
															stroke-width="2"
															stroke-miterlimit="10"
															stroke-linecap="round"
															stroke-linejoin="round"
														></path>
													</svg>
													<p
														class="text-white text-sm font-bold right-side-headline"
														>Bolt One-Click</p
													>
													<hr class="w-5 h-px bg-white opacity-35 mx-0 my-5" />
													<p
														class="text-white text-xs leading-2 opacity-75 mb-2 font-medium"
														>Bolt One-Click<br />adoption rates create an
														instant connection with the most valuable customers
														in our network.</p
													>
													<div
														style="color: #68d8fc"
														class="w-40 uppercase flex justify-start items-center text-xs mb-2 font-bold py-2 platform-text"
													>
														Learn More
														<svg
															class="ml-5 mb-4 platform-menu-graphic opacity-0"
															width="8"
															height="8"
															viewBox="0 0 8 8"
															fill="none"
															xmlns="http://www.w3.org/2000/svg"
														>
															<path
																d="M7.67331 4.31763C7.83806 4.15288 7.83806 3.88576 7.67331 3.72101L4.98852 1.03621C4.82376 0.871459 4.55665 0.871459 4.39189 1.03621C4.22714 1.20096 4.22714 1.46808 4.39189 1.63283L6.77838 4.01932L4.39189 6.4058C4.22714 6.57056 4.22714 6.83767 4.39189 7.00242C4.55665 7.16718 4.82376 7.16718 4.98852 7.00242L7.67331 4.31763ZM0.625 4.44119H7.375V3.59744H0.625V4.44119Z"
																fill="#68D8FC"
															></path>
														</svg>
													</div>
												</a>

												<a
													href=""
													class="block relative py-2 px-5 mt-5 platform-rail-link"
												>
													<svg
														class="absolute opacity-25 platform-icon"
														style="top: 20px; right: 14px"
														width="41"
														height="45"
														viewBox="0 0 41 45"
														fill="none"
														xmlns="http://www.w3.org/2000/svg"
													>
														<path
															d="M22.7052 1.70909C23.0968 1.31967 23.0986 0.686507 22.7091 0.294885C22.3197 -0.0967361 21.6865 -0.0985173 21.2949 0.290907L22.7052 1.70909ZM19.8787 3.10942L19.1736 2.40032L18.4605 3.10942L19.1736 3.81851L19.8787 3.10942ZM21.2949 5.92793C21.6865 6.31735 22.3197 6.31557 22.7091 5.92395C23.0986 5.53233 23.0968 4.89917 22.7052 4.50974L21.2949 5.92793ZM18.588 43.2909C18.1964 43.6803 18.1946 44.3135 18.584 44.7051C18.9734 45.0967 19.6066 45.0985 19.9982 44.7091L18.588 43.2909ZM21.4144 41.8906L22.1195 42.5997L22.8326 41.8906L22.1195 41.1815L21.4144 41.8906ZM19.9982 39.0721C19.6066 38.6826 18.9734 38.6844 18.584 39.0761C18.1946 39.4677 18.1964 40.1008 18.588 40.4903L19.9982 39.0721ZM20.5 2.10942C19.9477 2.10942 19.5 2.55713 19.5 3.10942C19.5 3.6617 19.9477 4.10942 20.5 4.10942V2.10942ZM24.7713 40.3982C24.2337 40.5245 23.9002 41.0627 24.0265 41.6004C24.1528 42.138 24.691 42.4715 25.2287 42.3452L24.7713 40.3982ZM16.2287 4.60179C16.7663 4.4755 17.0998 3.93727 16.9735 3.39962C16.8472 2.86197 16.309 2.52849 15.7713 2.65478L16.2287 4.60179ZM0.537548 27.1579C0.663879 27.6956 1.20213 28.029 1.73978 27.9027C2.27742 27.7764 2.61085 27.2381 2.48452 26.7005L0.537548 27.1579ZM3.74606 34.2531C4.06588 34.7033 4.69015 34.8091 5.14041 34.4893C5.59067 34.1695 5.69642 33.5452 5.3766 33.0949L3.74606 34.2531ZM3.33919 29.3835C3.1313 28.8718 2.54798 28.6256 2.03632 28.8335C1.52466 29.0414 1.27841 29.6247 1.4863 30.1363L3.33919 29.3835ZM9.26563 39.5587C9.72809 39.8606 10.3477 39.7304 10.6496 39.268C10.9515 38.8055 10.8214 38.1858 10.3589 37.8839L9.26563 39.5587ZM7.21748 35.3011C6.83184 34.9058 6.19873 34.8979 5.80338 35.2836C5.40803 35.6692 5.40017 36.3023 5.78581 36.6977L7.21748 35.3011ZM12.7885 39.2219C12.2882 38.9881 11.693 39.2041 11.4592 39.7045C11.2254 40.2048 11.4414 40.8 11.9417 41.0338L12.7885 39.2219ZM18.6301 22.0351L19.6084 22.2422C19.7039 21.7911 19.4786 21.3332 19.0629 21.1336L18.6301 22.0351ZM16.7602 30.8672L15.7819 30.6601C15.7194 30.9551 15.7935 31.2625 15.9833 31.4968C16.1732 31.7311 16.4587 31.8672 16.7602 31.8672V30.8672ZM24.7072 30.8672V31.8672C25.0176 31.8672 25.3103 31.7231 25.4996 31.4772C25.6889 31.2312 25.7533 30.9114 25.6739 30.6113L24.7072 30.8672ZM22.3699 22.0351L21.9741 21.1167C21.5193 21.3127 21.2764 21.8121 21.4031 22.2909L22.3699 22.0351ZM34.5 22.5C34.5 30.1802 28.2373 36.4158 20.5 36.4158V38.4158C29.3312 38.4158 36.5 31.2954 36.5 22.5H34.5ZM20.5 36.4158C12.7627 36.4158 6.5 30.1802 6.5 22.5H4.5C4.5 31.2954 11.6688 38.4158 20.5 38.4158V36.4158ZM6.5 22.5C6.5 14.8198 12.7627 8.58417 20.5 8.58417V6.58417C11.6688 6.58417 4.5 13.7046 4.5 22.5H6.5ZM20.5 8.58417C28.2373 8.58417 34.5 14.8198 34.5 22.5H36.5C36.5 13.7046 29.3312 6.58417 20.5 6.58417V8.58417ZM21.2949 0.290907L19.1736 2.40032L20.5838 3.81851L22.7052 1.70909L21.2949 0.290907ZM19.1736 3.81851L21.2949 5.92793L22.7052 4.50974L20.5838 2.40032L19.1736 3.81851ZM19.9982 44.7091L22.1195 42.5997L20.7093 41.1815L18.588 43.2909L19.9982 44.7091ZM22.1195 41.1815L19.9982 39.0721L18.588 40.4903L20.7093 42.5997L22.1195 41.1815ZM20.5 4.10942C30.7226 4.10942 39 12.3485 39 22.5H41C41 11.2333 31.8165 2.10942 20.5 2.10942V4.10942ZM39 22.5C39 31.1908 32.9333 38.481 24.7713 40.3982L25.2287 42.3452C34.2669 40.2222 41 32.1472 41 22.5H39ZM2 22.5C2 13.8092 8.06668 6.51897 16.2287 4.60179L15.7713 2.65478C6.73312 4.77778 0 12.8528 0 22.5H2ZM2.48452 26.7005C2.16774 25.3523 2 23.9463 2 22.5H0C0 24.1014 0.185799 25.661 0.537548 27.1579L2.48452 26.7005ZM5.3766 33.0949C4.56144 31.9473 3.87541 30.7032 3.33919 29.3835L1.4863 30.1363C2.08147 31.6011 2.84253 32.981 3.74606 34.2531L5.3766 33.0949ZM10.3589 37.8839C9.21772 37.1389 8.16428 36.2718 7.21748 35.3011L5.78581 36.6977C6.83454 37.7728 8.00139 38.7333 9.26563 39.5587L10.3589 37.8839ZM21.3731 40.8914C18.1914 41.023 14.9944 40.2528 12.7885 39.2219L11.9417 41.0338C14.4222 42.193 17.9368 43.0353 21.4558 42.8897L21.3731 40.8914ZM25.7072 18.3163C25.7072 15.481 23.3376 13.1327 20.5 13.1327V15.1327C22.2436 15.1327 23.7072 16.5962 23.7072 18.3163H25.7072ZM20.5 13.1327C17.6624 13.1327 15.2928 15.481 15.2928 18.3163H17.2928C17.2928 16.5962 18.7564 15.1327 20.5 15.1327V13.1327ZM15.2928 18.3163C15.2928 20.3435 16.5093 22.1263 18.1973 22.9366L19.0629 21.1336C18.0396 20.6424 17.2928 19.5431 17.2928 18.3163H15.2928ZM17.6518 21.828L15.7819 30.6601L17.7385 31.0743L19.6084 22.2422L17.6518 21.828ZM16.7602 31.8672H24.7072V29.8672H16.7602V31.8672ZM25.6739 30.6113L23.3366 21.7793L21.4031 22.2909L23.7405 31.123L25.6739 30.6113ZM22.7656 22.9535C24.5648 22.1782 25.7072 20.3088 25.7072 18.3163H23.7072C23.7072 19.5778 22.9798 20.6834 21.9741 21.1167L22.7656 22.9535Z"
															fill="white"
														></path>
													</svg>
													<p
														class="text-white text-sm font-bold right-side-headline"
														>SSO</p
													>
													<hr class="w-5 h-px bg-white opacity-30 mx-0 my-4" />
													<p
														class="text-white text-xs leading-2 opacity-75 mb-2 font-medium right-side-copy"
														>SSO Commerce<br />redefines the login layer for
														commerce and increases account registrations for
														retailers.</p
													>
													<div
														style="color: #68d8fc"
														class="w-40 uppercase flex justify-start items-center text-xs mb-4 font-bold py-8 platform-text"
													>
														Learn More
														<svg
															class="ml-5 mb-4 platform-menu-graphic opacity-0"
															width="8"
															height="8"
															viewBox="0 0 8 8"
															fill="none"
															xmlns="http://www.w3.org/2000/svg"
														>
															<path
																d="M7.67331 4.31763C7.83806 4.15288 7.83806 3.88576 7.67331 3.72101L4.98852 1.03621C4.82376 0.871459 4.55665 0.871459 4.39189 1.03621C4.22714 1.20096 4.22714 1.46808 4.39189 1.63283L6.77838 4.01932L4.39189 6.4058C4.22714 6.57056 4.22714 6.83767 4.39189 7.00242C4.55665 7.16718 4.82376 7.16718 4.98852 7.00242L7.67331 4.31763ZM0.625 4.44119H7.375V3.59744H0.625V4.44119Z"
																fill="#68D8FC"
															></path>
														</svg>
													</div>
												</a>
											</div>
										</div>
									</div>
								</div>
							</div>
							<!-- dropdown -->
						</div>

						<li class="nav-item">
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

<style scoped>
.col2 {
	background: linear-gradient(173.68deg, #000000 1.3%, rgba(0, 0, 0, 0) 78.42%),
		linear-gradient(349.4deg, #133ee3 -35.81%, #7532e1 61.27%);
}
</style>
<script>
export default {
	name: 'pink-navbar',
	name: 'large-modal',
	data() {
		return {
			showMenu: false,
			showModal: false,
			navDropDown: false,
		};
	},
	methods: {
		toggleNavbar: function () {
			this.showMenu = !this.showMenu;
		},
		toggleModal: function () {
			this.showModal = !this.showModal;
		},
		showDropDown: function () {
			this.navDropDown = !this.navDropDown;
		},
	},
};
</script>
