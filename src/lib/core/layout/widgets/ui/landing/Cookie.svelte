<script>
	let hideCookie = true;
</script>

{#if hideCookie}
	<section
		class="hidden-sm  fixed  left-4 bottom-6 z-10 mx-auto max-w-md rounded-2xl border border-gray-200 bg-gradient-to-l from-pink-500 to-pink-600  p-4 backdrop-blur-[30px] "
	>
		<h2 class="font-semibold text-white ">🍪 Cookie Notice</h2>

		<p class="mt-4 text-sm text-gray-100 ">
			We use cookies to ensure that we give you the best experience on our website. <a
				href="#"
				class="text-pink-800 hover:underline">Read cookies policies</a
			>.
		</p>

		<div class="mt-4 flex shrink-0 items-center justify-between gap-x-4">
			<button
				class="text-xs text-gray-200 underline transition-colors duration-100 hover:text-white focus:outline-none "
			>
				Manage your preferences
			</button>

			<button
				on:click={() => (hideCookie = !hideCookie)}
				class=" rounded-lg bg-pink-700 px-4 py-2.5 text-xs font-medium text-white transition-colors duration-300 hover:bg-gray-700 focus:outline-none"
			>
				Accept
			</button>
		</div>
	</section>
{/if}

<style>
	@media (max-width: 640px) {
		.hidden-sm {
			display: none;
		}
	}
</style>
