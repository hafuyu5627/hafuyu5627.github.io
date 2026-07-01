<script lang="ts">
	import { page } from '$app/state';
	let { msg = page.error!.message, status = page.status.toString() } = $props()
</script>

<div class="flex flex-col h-full">
	<div class="flex flex-col gap-[3%] items-center justify-center bg-blue-300 [flex:4]">
		<div class="text-blue-700 font-bold text-7xl xl:text-9xl">
			{status}
		</div>

		<div class="font-bold text-3xl xl:text-7xl lg:text-6xl md:text-5xl">
			{msg}
		</div>
	</div>
	<footer class="bg-blue-200 hover:bg-blue-100 flex-1 text-center relative flex text-gray-950 hover:text-gray-500 transition-colors">
		<a class="text-3xl flex-1 content-center" href="/">返回主頁</a>
	</footer>
</div>
