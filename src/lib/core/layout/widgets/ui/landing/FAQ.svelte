<script>
	const faq = [
		{
			categoryTitle: 'Lorem ipsum is placeholder text ',
			content: [
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				}
			]
		},
		{
			categoryTitle: 'Lorem ipsum is placeholder text ',
			content: [
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				}
			]
		},
		{
			categoryTitle: 'Lorem ipsum is placeholder text ',
			content: [
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				},
				{
					title: 'Lorem ipsum is placeholder text ',
					desc: [
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.',
						'Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.'
					]
				}
			]
		}
	];

	$: selectedCategory = [faq[0].content];
</script>

<section class="py-12 ">
	<div class="container mx-auto min-h-screen w-full rounded-r-xl bg-gray-200 px-24 py-12 lg:mr-32">
		<h2
			class="mt-2 text-center text-4xl font-bold leading-none tracking-tighter text-neutral-600 md:text-7xl lg:text-5xl"
		>
			Have any Questions?
		</h2>

		<div class="mt-8 lg:-mx-12 lg:flex xl:mt-16">
			<div class="lg:mx-12">
				<h1 class="text-xl font-semibold text-gray-800 ">Table of Content</h1>

				<div class="mt-4 space-y-4 lg:mt-8">
					{#each faq as toc}
						<button
							on:click={() => (selectedCategory = toc.content)}
							class="block text-pink-500 hover:underline ">{toc.categoryTitle}</button
						>
					{/each}
				</div>
			</div>

			<a name="faq" />
			<div class="mt-8 flex-1 lg:mx-12 lg:mt-0">
				{#each selectedCategory as answers}
					<div>
						<button class="flex items-center focus:outline-none">
							<svg
								class="h-6 w-6 flex-shrink-0 text-pink-500"
								fill="none"
								stroke="currentColor"
								viewBox="0 0 24 24"
								xmlns="http://www.w3.org/2000/svg"
								><path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M20 12H4"
								/></svg
							>

							<svg
								xmlns="http://www.w3.org/2000/svg"
								class="h-6 w-6 flex-shrink-0 text-pink-500"
								fill="none"
								viewBox="0 0 24 24"
								stroke="currentColor"
							>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M12 4v16m8-8H4"
								/>
							</svg>

							<h1 class="mx-4 text-xl text-gray-700 ">
								{answers.title}
							</h1>
						</button>

						<div class="mt-8 flex md:mx-10">
							<span class="border border-pink-500" />

							<p class="max-w-3xl px-4 text-gray-500 ">
								{answers.desc}
							</p>
						</div>
					</div>

					<hr class="my-8 border-gray-200 " />
				{/each}
			</div>
		</div>
	</div>
</section>
