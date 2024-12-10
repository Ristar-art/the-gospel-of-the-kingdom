<script lang="ts">
	import Sidebar from "./Sidebar.svelte";
	import Dashboard from "./Dashboard.svelte";
	let Courses ;
	let Users;
	let Settings;

	// State to control sidebar visibility on mobile
	let isSidebarOpen: boolean = $state(false);

	// State to control which view to display (dashboard or courses)
	let currentView: string =$state( "dashboard");

	/** Toggle sidebar visibility */
	const toggleSidebar = () => {
		isSidebarOpen = !isSidebarOpen;
	};

	/** Set the current view */
	const setView = (view: string) => {		
		currentView = view;
	};
	// Mapping of view names to their corresponding components
const viewComponents = {
    dashboard: Dashboard,
    courses: Courses,
    users: Users,
    settings: Settings,
};
</script>

<svelte:head>
    <title>Home</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="flex h-screen bg-gray-100">
    <!-- Sidebar component -->
    <Sidebar {isSidebarOpen} {toggleSidebar} {setView} />

    <!-- Main content -->
    <main class="flex-1 overflow-x-hidden overflow-y-auto">
        {#if currentView in viewComponents}
            <svelte:component this={viewComponents[currentView]} />
        {:else}
            <p>View not found</p>
        {/if}
    </main>

</div>