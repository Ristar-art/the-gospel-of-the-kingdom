<script lang="ts">
    import { Home, Users, Book, Settings, Menu, X } from "lucide-svelte";

    export let isSidebarOpen: boolean;
    export let toggleSidebar: () => void;
    export let setView: (view: string) => void;

    const navItems = [
        { icon: Home, label: "Dashboard", view: "dashboard" },
        { icon: Users, label: "Users", view: "users" },
        { icon: Book, label: "Courses", view: "courses" },
        { icon: Settings, label: "Settings", view: "settings" },
    ];
</script>

<div class="sidebar flex h-screen" class:open={isSidebarOpen}>
    <aside class="fixed inset-y-0 left-0 z-30 w-64 transform bg-white shadow-lg transition-transform duration-300 ease-in-out lg:static lg:translate-x-0 {isSidebarOpen ? 'translate-x-0' : '-translate-x-full'}">
        <div class="flex h-full flex-col">
            <div class="flex items-center justify-between border-b px-4 py-3">
                <span class="text-xl font-semibold">Dashboard</span>
                <button class="lg:hidden" on:click={toggleSidebar}>
                    {#if isSidebarOpen}
                        <X size={24} />
                    {:else}
                        <Menu size={24} />
                    {/if}
                </button>
            </div>

            <nav class="flex-1 space-y-1 px-2 py-4">
                {#each navItems as item}
                    <a 
                        href={`#${item.view}`} 
                        class="flex items-center rounded-lg px-4 py-2 text-gray-600 hover:bg-gray-100"
                        on:click={() => setView(item.view)}
                    >
                        <svelte:component this={item.icon} size={20} class="mr-3" />
                        {item.label}
                    </a>
                {/each}
            </nav>

            <div class="border-t p-4">
                <div class="flex items-center">
                    <img src="$assets/ui-user.png" alt="User" class="h-8 w-8 rounded-full" />
                    <div class="ml-3">
                        <p class="text-sm font-medium">John Doe</p>
                        <p class="text-xs text-gray-500">admin@example.com</p>
                    </div>
                </div>
            </div>
        </div>
    </aside>
</div>