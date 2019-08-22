<template>
    <div class="layout">
		<nav class="bg-gray-800 p-2 mt-0 fixed w-full z-10 top-0">
			<div class="container mx-auto flex flex-wrap items-center">
				<div class="flex w-full md:w-1/2 justify-center md:justify-start text-white font-extrabold">
					<g-link class="text-white no-underline hover:text-white hover:no-underline text-2xl font-semibold" to="/">{{ $static.metaData.siteName }}</g-link>
				</div>
				<div class="flex w-full content-center justify-between md:w-1/2 md:justify-end">
					<ul class="list-reset flex justify-between flex-1 md:flex-none items-center">
						<li class="mr-3">
							<g-link class="inline-block py-2 px-4 text-white no-underline" to="/">Home</g-link>
						</li>
					</ul>
				</div>
			</div>
		</nav>
        <header class="flex">
            <strong>
                <g-link to="/">{{ $static.metaData.siteName }}</g-link>
            </strong>
        </header>
        <slot />
    </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style>
    /* body {
        font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI",
            Roboto, "Helvetica Neue", Arial, sans-serif;
        margin: 0;
        padding: 0;
        line-height: 1.5;
    }

    .layout {
        max-width: 760px;
        margin: 0 auto;
        padding-left: 20px;
        padding-right: 20px;
    }

    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        height: 80px;
    }

    .nav__link {
        margin-left: 20px;
    } */
</style>
