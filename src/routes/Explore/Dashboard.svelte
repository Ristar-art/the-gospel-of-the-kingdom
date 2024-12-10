<script lang="ts">
	import { Menu } from "lucide-svelte";

	// Props
	let stats = [
		{ title: "Total Courses", value: "150" },
		{ title: "Total Enrollments", value: "2,345" },
		{ title: "Active Courses", value: "75" },
		{ title: "Pending Reviews", value: "10" },
	];
</script>

<div class="p-6">
	<!-- Header -->
	<div class="mb-8 flex items-center justify-between">
		<h1 class="text-2xl font-semibold">Dashboard Overview</h1>
		<button class="lg:hidden">
			<Menu size={24} />
		</button>
	</div>

	<!-- Stats Grid -->
	<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-4">
		{#each stats as stat}
			<div class="rounded-lg bg-white p-6 shadow-sm">
				<h3 class="text-sm font-medium text-gray-500">{stat.title}</h3>
				<p class="mt-2 text-3xl font-semibold">{stat.value}</p>
			</div>
		{/each}
	</div>

	<!-- Recent Activity -->
	<div class="mt-8">
		<h2 class="mb-4 text-xl font-semibold">Recent Activity</h2>
		<div class="rounded-lg bg-white p-6 shadow-sm">
			<p class="text-gray-500">No recent activity to display.</p>
		</div>
	</div>
</div>