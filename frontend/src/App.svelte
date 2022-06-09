<script lang="ts">
    import Beach_Regular from "svelte-fluentui-icons/icons/Beach_Regular.svelte";
    import { GetName } from "../wailsjs/go/main/App.js";

    document.body.className = "antialiased bg-white text-slate-600 text-base";

    let name = "";
    let title = "";

    GetName().then(function (newName) {
        name = newName;
        title = name + " Template";
    });
</script>

<svelte:head>
    <title>{title}</title>
</svelte:head>

<div class="flex items-center h-screen place-content-center">
    <div class="flex flex-col items-center space-y-6">
        <Beach_Regular size={180} class="text-blue-600" />
        <h1 class="text-4xl font-bold">Hello {name}</h1>
        <p>Vite + Svelte + TS + Tailwindcss + {name}</p>
    </div>
</div>
