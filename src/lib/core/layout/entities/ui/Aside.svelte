<script>
	// import { ten, kanbanel, healthCheck, actionDelegation } from '../../../data/';

	// const productsList = [ten, kanbanel, healthCheck, actionDelegation];
	const icons = [
		{
			icon: '/cynefin/icon.svg',
			link: '/apps/cynefin'
		},
		{
			icon: '/action-delegation/icon.svg',
			link: '/apps/action-delegation'
		},
		{
			icon: 'health-check/icon.svg',
			link: '/apps/health-check'
		},
		{
			icon: '/kanbanel/icon.svg',
			link: '/apps/kanbanel'
		},
		{
			icon: '/lean-coffee/icon.svg',
			link: '/apps/lean-coffee'
		},
		{
			icon: '/pomodoro-plan/icon.svg',
			link: '/apps/pomodoro-plan/'
		},
		// {
		//   icon: '',
		//   link: '/apps/retromat'
		// },
		{
			icon: '/spiral-dynamics/icon.svg',
			link: '/apps/spiral-dynamics'
		},
		{
			icon: '/ten/icon.svg',
			link: '/apps/ten'
		},
		// {
		//   icon: '',
		//   link: '/apps/ten'
		// },
		// {
		//   icon: '',
		//   link: '/apps/ten'
		// },
		{
			icon: '/scrum-puzle/icon.svg',
			link: '/apps/scrum-puzle'
		}
	];

	export let selectedApp;
</script>

<aside class="flex">
	<div class="flex h-full min-h-screen w-16 flex-col items-center border-gray-700 bg-pink-800 py-8">
		<nav class="flex flex-1 flex-col items-center space-y-6 ">
			<!-- <a href="#">
				<img class="h-6 w-auto" src="https://merakiui.com/images/logo.svg" alt="" />
			</a> -->

			{#each icons as icon}
				<button
					on:click={() => selectedApp}
					class="focus:outline-nones inline-block rounded-lg p-1.5 text-black transition-colors duration-200 hover:bg-black"
				>
					<img src={icon.icon} class="h-8 w-8" alt="" />
				</button>
			{/each}

			<div class="mt-20 flex flex-col items-center space-y-4">
				<a href="#">
					<img
						class="h-8 w-8 rounded-lg object-cover"
						src="https://images.unsplash.com/photo-1531427186611-ecfd6d936c79?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&h=634&q=80"
						alt="avatar"
					/>
				</a>

				<a
					href="#"
					class="rotate-180 text-gray-500 transition-colors duration-200 hover:text-pink-500 rtl:rotate-0 dark:text-gray-400 dark:hover:text-pink-400"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="h-6 w-6"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15M12 9l-3 3m0 0l3 3m-3-3h12.75"
						/>
					</svg>
				</a>
			</div>
		</nav>
	</div>
	{#if selectedApp}
		<div
			class="h-full min-h-screen w-60 overflow-y-auto border-l border-r bg-white px-5 py-8 dark:border-gray-700 dark:bg-gray-900 sm:w-64"
		>
			<div class="relative">
				<span class="absolute inset-y-0 left-0 flex items-center pl-3">
					<svg class="h-5 w-5 text-gray-400" viewBox="0 0 24 24" fill="none">
						<path
							d="M21 21L15 15M17 10C17 13.866 13.866 17 10 17C6.13401 17 3 13.866 3 10C3 6.13401 6.13401 3 10 3C13.866 3 17 6.13401 17 10Z"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
					</svg>
				</span>

				<input
					type="text"
					class="w-full rounded-md border bg-white py-1.5 pl-10 pr-4 text-gray-700 focus:border-pink-400 focus:outline-none focus:ring focus:ring-pink-300 focus:ring-opacity-40 dark:border-gray-600 dark:bg-gray-900 dark:text-gray-300 dark:focus:border-pink-300"
					placeholder="Search"
				/>
			</div>

			<nav class="-mx-3 mt-4 space-y-6 ">
				<div class="space-y-3 ">
					<label class="px-3 text-xs uppercase text-gray-500 dark:text-gray-400">analytics</label>

					<a
						class="flex transform items-center rounded-lg px-3 py-2 text-gray-600 transition-colors duration-300 hover:bg-gray-100 hover:text-gray-700 dark:text-gray-200 dark:hover:bg-gray-800 dark:hover:text-gray-200"
						href="#"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="h-5 w-5"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M3.75 3v11.25A2.25 2.25 0 006 16.5h2.25M3.75 3h-1.5m1.5 0h16.5m0 0h1.5m-1.5 0v11.25A2.25 2.25 0 0118 16.5h-2.25m-7.5 0h7.5m-7.5 0l-1 3m8.5-3l1 3m0 0l.5 1.5m-.5-1.5h-9.5m0 0l-.5 1.5m.75-9l3-3 2.148 2.148A12.061 12.061 0 0116.5 7.605"
							/>
						</svg>

						<span class="mx-2 text-sm font-medium">Dashboard</span>
					</a>
				</div>

				<div class="space-y-3 ">
					<label class="px-3 text-xs uppercase text-gray-500 dark:text-gray-400">content</label>

					<a
						class="flex transform items-center rounded-lg px-3 py-2 text-gray-600 transition-colors duration-300 hover:bg-gray-100 hover:text-gray-700 dark:text-gray-200 dark:hover:bg-gray-800 dark:hover:text-gray-200"
						href="#"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="h-5 w-5"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M19.5 14.25v-2.625a3.375 3.375 0 00-3.375-3.375h-1.5A1.125 1.125 0 0113.5 7.125v-1.5a3.375 3.375 0 00-3.375-3.375H8.25m0 12.75h7.5m-7.5 3H12M10.5 2.25H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 00-9-9z"
							/>
						</svg>

						<span class="mx-2 text-sm font-medium">Guides</span>
					</a>

					<a
						class="flex transform items-center rounded-lg px-3 py-2 text-gray-600 transition-colors duration-300 hover:bg-gray-100 hover:text-gray-700 dark:text-gray-200 dark:hover:bg-gray-800 dark:hover:text-gray-200"
						href="#"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="h-5 w-5"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M10.343 3.94c.09-.542.56-.94 1.11-.94h1.093c.55 0 1.02.398 1.11.94l.149.894c.07.424.384.764.78.93.398.164.855.142 1.205-.108l.737-.527a1.125 1.125 0 011.45.12l.773.774c.39.389.44 1.002.12 1.45l-.527.737c-.25.35-.272.806-.107 1.204.165.397.505.71.93.78l.893.15c.543.09.94.56.94 1.109v1.094c0 .55-.397 1.02-.94 1.11l-.893.149c-.425.07-.765.383-.93.78-.165.398-.143.854.107 1.204l.527.738c.32.447.269 1.06-.12 1.45l-.774.773a1.125 1.125 0 01-1.449.12l-.738-.527c-.35-.25-.806-.272-1.203-.107-.397.165-.71.505-.781.929l-.149.894c-.09.542-.56.94-1.11.94h-1.094c-.55 0-1.019-.398-1.11-.94l-.148-.894c-.071-.424-.384-.764-.781-.93-.398-.164-.854-.142-1.204.108l-.738.527c-.447.32-1.06.269-1.45-.12l-.773-.774a1.125 1.125 0 01-.12-1.45l.527-.737c.25-.35.273-.806.108-1.204-.165-.397-.505-.71-.93-.78l-.894-.15c-.542-.09-.94-.56-.94-1.109v-1.094c0-.55.398-1.02.94-1.11l.894-.149c.424-.07.765-.383.93-.78.165-.398.143-.854-.107-1.204l-.527-.738a1.125 1.125 0 01.12-1.45l.773-.773a1.125 1.125 0 011.45-.12l.737.527c.35.25.807.272 1.204.107.397-.165.71-.505.78-.929l.15-.894z"
							/>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
							/>
						</svg>

						<span class="mx-2 text-sm font-medium">FAQ </span>
					</a>

					<a
						class="flex transform items-center rounded-lg px-3 py-2 text-gray-600 transition-colors duration-300 hover:bg-gray-100 hover:text-gray-700 dark:text-gray-200 dark:hover:bg-gray-800 dark:hover:text-gray-200"
						href="#"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="h-5 w-5"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M10.343 3.94c.09-.542.56-.94 1.11-.94h1.093c.55 0 1.02.398 1.11.94l.149.894c.07.424.384.764.78.93.398.164.855.142 1.205-.108l.737-.527a1.125 1.125 0 011.45.12l.773.774c.39.389.44 1.002.12 1.45l-.527.737c-.25.35-.272.806-.107 1.204.165.397.505.71.93.78l.893.15c.543.09.94.56.94 1.109v1.094c0 .55-.397 1.02-.94 1.11l-.893.149c-.425.07-.765.383-.93.78-.165.398-.143.854.107 1.204l.527.738c.32.447.269 1.06-.12 1.45l-.774.773a1.125 1.125 0 01-1.449.12l-.738-.527c-.35-.25-.806-.272-1.203-.107-.397.165-.71.505-.781.929l-.149.894c-.09.542-.56.94-1.11.94h-1.094c-.55 0-1.019-.398-1.11-.94l-.148-.894c-.071-.424-.384-.764-.781-.93-.398-.164-.854-.142-1.204.108l-.738.527c-.447.32-1.06.269-1.45-.12l-.773-.774a1.125 1.125 0 01-.12-1.45l.527-.737c.25-.35.273-.806.108-1.204-.165-.397-.505-.71-.93-.78l-.894-.15c-.542-.09-.94-.56-.94-1.109v-1.094c0-.55.398-1.02.94-1.11l.894-.149c.424-.07.765-.383.93-.78.165-.398.143-.854-.107-1.204l-.527-.738a1.125 1.125 0 01.12-1.45l.773-.773a1.125 1.125 0 011.45-.12l.737.527c.35.25.807.272 1.204.107.397-.165.71-.505.78-.929l.15-.894z"
							/>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
							/>
						</svg>

						<span class="mx-2 text-sm font-medium">Setting</span>
					</a>
				</div>
			</nav>
		</div>
	{/if}
</aside>
