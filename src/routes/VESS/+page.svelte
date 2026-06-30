<script lang="ts">
    const extraMods: {
        name: string,
        version: string,
        targetVersion?: string,
        feature: string,
        note?: string,
    }[] = [
        {
            name: "ReplayMod",
            version: "2.6.25",
            feature: "Replay",
        },
        {
            name: "Iris Shaders",
            version: "1.10.4",
            feature: "Shader Enhancement",
        },
        {
            name: "Sodium",
            version: "0.8.2",
            feature: "Performance Improvement",
        },
        {
            name: "Alternate Current",
            version: "1.9.0",
            feature: "Performance Improvement",
        },
        {
            name: "Apple Skin",
            version: "3.0.7",
            feature: "Food QoL",
        },
        {
            name: "Ambient Environment",
            version: "27.0.0.1",
            feature: "Rendering QoL",
        },
        {
            name: "BadOptimizations",
            version: "2.4.1",
            feature: "Performance Improvement",
        },
        {
            name: "Better Advancements",
            version: "0.4.8.51",
            feature: "Feature GUI QoL",
        },
        {
            name: "ImmediatelyFast",
            version: "1.14.1",
            feature: "Performance Improvement",
        },
        {
            name: "Lithium",
            version: "0.21.2",
            feature: "Performance Improvement",
        },
        {
            name: "ModernFix",
            version: "5.25.2-build.4",
            feature: "Bug Fixes",
        },
        {
            name: "Mouse Tweaks",
            version: "2.30",
            feature: "Mouse Functionalities",
        },
        {
            name: "Not Enough Animations",
            version: "1.11.1",
            feature: "Rendering QoL",
        },
        {
            name: "Cloth Config API",
            version: "21.11.153",
            feature: "Configs",
        },
        {
            name: "Sound Physics Remastered",
            version: "1.5.1",
            feature: "Audio QoL",
        },
        {
            name: "Sodium Extra",
            version: "0.8.3",
            feature: "Sodium Configs",
        },
        {
            name: "Better Statistics Screen",
            version: "5.0.0-beta.2",
            feature: "Feature GUI QoL",
        },
        {
            name: "BetterF3",
            version: "17.0.0",
            targetVersion: "1.21.10",
            feature: "Feature GUI QoL",
        },
        {
            name: "Distant Horizons",
            version: "2.4.5-b",
            feature: "Distant Chunk Rendering",
        },
        {
            name: "Shulker Box Tooltip",
            version: "5.2.14",
            feature: "Feature GUI QoL",
        },
        {
            name: "Just Enough Items (JEI)",
            version: "27.4.0.15",
            feature: "Recipe Viewer",
        },
        {
            name: "Just Enough Professions (JEP)",
            version: "10.0.0",
            feature: "JEI Addon",
        },
        {
            name: "Just Enough Resources (JER)",
            version: "1.8.1.28",
            targetVersion: "1.21.10",
            feature: "JEI Addon",
            note: "無法運作"
        },
        {
            name: "Visual Workbench",
            version: "21.11.1",
            feature: "Crafting Improvement",
        },
        {
            name: "JourneyMap",
            version: "6.0.0-beta.54",
            feature: "Minimap",
        },
        {
            name: "Durability Tooltip",
            version: "1.1.6",
            feature: "Feature GUI QoL",
        },
        {
            name: "Trade Cycling",
            version: "1.0.20",
            feature: "Trading Aid",
        },
        {
            name: "Concurrent Chunk Management Engine",
            version: "0.3.6.0.0",
            feature: "Performance Improvement",
        },
        {
            name: "FerriteCore (Fabric)",
            version: "8.0.3",
            feature: "Performance Improvement",
        },
        {
            name: "<s>Armor Durability HUD</s>",
            version: "8.1.1.3",
            feature: "Feature GUI QoL",
            note: "似乎需要JavaFX<sup>1</sup>"
        },
        {
            name: "Better Than Mending",
            version: "2.2.5",
            feature: "Self Mending",
        },
        {
            name: "Inventory Profiles Next",
            version: "2.2.3",
            feature: "Inventory Management",
        },
        {
            name: "Wall-Jump TXF",
            version: "1.3.5",
            feature: "Wall Jump",
        },
        {
            name: "<s>Enchantment Descriptions</s>",
            version: "21.10.2",
            targetVersion: "1.21.10",
            feature: "Feature GUI QoL",
            note: "不支援"
        },
        {
            name: "Clumps",
            version: "29.0.0.1",
            feature: "Performance Improvement",
        },
        {
            name: "Spyglass Improvements",
            version: "1.5.12-beta",
            feature: "Spyglass Improvement",
        },
        {
            name: "AmbientSounds 6",
            version: "6.3.3",
            feature: "BGM Improvement",
        },
        {
            name: "Architectury API",
            version: "19.0.1",
            feature: "Core Lib",
        },
        {
            name: "TCDCommons API",
            version: "5.0.0-beta.1",
            feature: "Core Lib",
        },
        {
            name: "SuperMartijn642's Config Lib",
            version: "1.1.8",
            feature: "Core Lib",
        },
        {
            name: "Forge Config API Port",
            version: "21.11.1",
            feature: "Core Lib",
        },
        {
            name: "Puzzles Lib",
            version: "21.11.4",
            feature: "Core Lib",
        },
        {
            name: "Fabric API",
            version: "0.141.1",
            feature: "Fabric Core",
            note: "取代更新"
        },
        {
            name: "Inventory HUD+",
            version: "3.4.29",
            feature: "Feature GUI QoL",
        },
        {
            name: "Reese's Sodium Options",
            version: "2.0.2",
            feature: "Sodium Configs",
        },
        {
            name: "Controlling",
            version: "29.0.1",
            feature: "Settings Addon",
        },
        {
            name: "Searchables",
            version: "1.0.2",
            feature: "Core Lib",
        },
        {
            name: "BetterGrassify",
            version: "1.8.3",
            feature: "Rendering QoL",
        },
        {
            name: "Pro Placer",
            version: "21.11.0",
            feature: "Building Aid",
        },
        {
            name: "MiniHUD",
            version: "0.38.2",
            feature: "Feature GUI QoL",
        },
        {
            name: "LambDynamicLights",
            version: "4.9.1",
            feature: "Rendering QoL",
        },
        {
            name: "MaLiLib",
            version: "0.27.3",
            feature: "Core Lib",
        },
        {
            name: "CreativeCore",
            version: "2.14.9",
            feature: "Core Lib",
        },
        {
            name: "Cubes Without Borders",
            version: "3.0.0-build.14",
            feature: "Rendering QoL",
        },
        {
            name: "<s>More Overlays Updated</s>",
            version: "1.24.1",
            targetVersion: "1.21.10",
            feature: "Feature GUI QoL",
        },
        {
            name: "<s>oωo</s>",
            version: "0.12.24",
            targetVersion: "1.21.10",
            feature: "Core Lib",
        },
        {
            name: "libIPN",
            version: "6.6.2",
            feature: "Core Lib",
        },
        {
            name: "Fabric Language Kotlin",
            version: "2.3.0",
            feature: "Core Lib",
        },
        {
            name: "Untranslated Items",
            version: "1.15",
            feature: "Feature GUI QoL",
        },
        {
            name: "Ladders Don't Suck",
            version: "1.0",
            feature: "Movement QoL",
        }
    ];
	const disabledMods = { // From TVE
		"Compact Help Command": "Not useful",
		"Current Game Music Track": "Not useful anymore (music not played)",
		"Easy Elevators": "Not suitable",
		"Enchanting Commands": "Not useful",
		"Hand Over Your Items": "Not useful",
		"Recipe Commands": "Not useful",
		"Set World Spawn Point": "Not useful",
		"Superflat World No Slimes": "Not useful",
	};
	const resourcePacks = [
		"Low On Fire",
		"Low Shield",
		"Vanilla Experience+",
		"GUI Experience+",
	]
	const shaders = {
		"Complementary Shaders - Reimagined": "r5.6.1-1.21.11"
	}
	type NonEmptyArray<T> = [T, ...T[]];
	type NonEmptyRecord<K extends keyof any, T> = Record<K, T> & { [P in K]: T };
</script>

<h1 class="banner">原體生存</h1>

<div class="content">
    <p class="text-3xl">
        原味體驗生存(原體生存)系列會類似一般的原味生存持續連載，有各種模組作生存輔助，更進一步豐富原味生存體驗。
    </p>
    <p class="text-3xl">
        在這系列中我會做各種生存目標和建設，包括一般原味生存會做的事情。
    </p>
    <p class="text-2xl">
        此系列所使用的模組基於 The Vanilla Experience | TVE (CurseForge/Modrinth) 模組包另外修改和擴充，盡量更新到最新 Minecraft 版本。
    </p>
    <p class="text-2xl">
        所使用的模組、資源包和光影包如下：
    </p>
    <div class="pl-8">
        <p>模組：</p>
        <div class="pl-8">
            <p>基於 TVE 版本 1.21.11-7.31 	及以下：</p>
			<div class="pl-8">
				<style lang="scss">
					/** Rounded borders thanks to https://stackoverflow.com/a/4932321 */
					table {
						@apply border-spacing-0 border-[1px] border-separate border-solid border-black rounded-xl w-full;
					}

					th, td {
						@apply p-1;
						border-left: 1px solid black;
						border-top: 1px solid black;
					}

					th {
						@apply bg-slate-400;
						border-top: none;
					}

					th:first-child {
						@apply rounded-tl-xl;
					}

					th:last-child {
						@apply rounded-tr-xl;
					}

					tr:last-child {
						&>td:first-child {
							@apply rounded-bl-xl;
						}

						&>td:last-child {
							@apply rounded-br-xl;
						}
					}

					td:first-child, th:first-child {
						border-left: none;
					}

					tbody tr:nth-child(even) {
						@apply bg-gray-200;
					}

					tbody tr:nth-child(odd) {
						@apply bg-gray-50;
					}
				</style>
				<table>
					<thead>
						<tr>
							<th>模組</th>
							<th>版本</th>
							<th>目標版本</th>
							<th>功能</th>
							<th>註記</th>
						</tr>
					</thead>
					<tbody>
						{#each extraMods as mod}
						<tr>
							<td>{@html mod.name}</td>
							<td>{@html mod.version}</td>
							<td>{#if mod.targetVersion === undefined}&mdash;{:else}{@html mod.targetVersion}{/if}</td>
							<td>{@html mod.feature}</td>
							<td>{#if mod.note !== undefined}{@html mod.note}{/if}</td>
						</tr>
						{/each}
					</tbody>
				</table>
				<p>注：如"目標版本"無指定則模組最高標注支援版本為現時 Minecraft 版本。</p>
				<p><sup>1</sup>JavaFX 安裝極為麻煩，且模組主頁沒有寫需要 JavaFX。</p>
				<p>停用模組 (TVE):</p>
				<ul class="list-disc pl-12 text-lg">
					{#each Object.entries(disabledMods) as mod}
					<li>{mod[0]}: {mod[1]}</li>
					{/each}
				</ul>
			</div>
        </div>
		<p>資源包：</p>
		<ul class="list-disc pl-12 text-lg">
			{#each resourcePacks as pack}
			<li>{pack}</li>
			{/each}
		</ul>
		<p>光影包：</p>
		<ul class="list-disc pl-12 text-lg">
			{#each Object.entries(shaders) as shader}
			<li>{shader[0]}: {shader[1]}</li>
			{/each}
		</ul>
    </div>
	<br/>
	<p>更新紀錄：</p>
	<div class="pl-8">
		<!-- Title must in format of "[Pre|Mid]-EP<N>"; it is unreasonable to use "Post" -->
		{#snippet record(title: `${"Pre"|"Mid"}-EP${number}`, entries: NonEmptyArray<(
			["one", import("svelte").Snippet<[any]>, any] |
			["two", import("svelte").Snippet<[any, any]>, [any, any]] |
			["three", import("svelte").Snippet<[any, any, any]>, [any, any, any]]
		)>)}
			<!-- Better of this can support array of <() => snippet(args)>;
			     also sadly using generics in snippet function signature generate errors -->
			<p>{title}</p>
			<ul class="list-disc pl-12 text-lg">
				{#each entries as e}
				{#if e[0] === "one"}
				{@render e[1](e[2])}
				{:else if e[0] === "two"}
				{@render e[1](e[2][0], e[2][1])}
				{:else if e[0] === "three"}
				{@render e[1](e[2][0], e[2][1], e[2][2])}
				{/if}
				{/each}
			</ul>
		{/snippet}
		{#snippet listValues(lead: string, values: string[])}
			<li>
				{lead}
				<ul class="list-[circle] pl-12 text-lg">
					{#each values as v}
					<li>{v}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet addedMods(mods: NonEmptyArray<string>)}
			<li>
				Added mod{ mods.length > 1 ? "s" : "" }:
				<ul class="list-[circle] pl-12 text-lg">
					{#each mods as mod}
					<li>{mod}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet addedModsWithNote(mods: NonEmptyArray<string>, note: string)}
			<li>
				Added mod{ mods.length > 1 ? "s" : "" }:
				<div><small class="pl-4 italic">{@html note}</small></div>
				<ul class="list-[circle] pl-12 text-lg">
					{#each mods as mod}
					<li>{mod}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet updatedMods(mods: NonEmptyRecord<string, {from: string; to: string}>)}
			<li>
				Updated mod{ Object.keys(mods).length > 1 ? "s" : "" }:
				<ul class="list-[circle] pl-12 text-lg">
					{#each Object.entries(mods) as mod}
					<li>{mod[0]}: {mod[1].from} &xrArr; {mod[1].to}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet startedDisablingMods(mods: NonEmptyArray<string>)}
			<li>
				Started disabling mod{ mods.length > 1 ? "s" : "" }:
				<ul class="list-[circle] pl-12 text-lg">
					{#each mods as mod}
					<li>{mod}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet disabledMoreMods(mods: NonEmptyArray<string>)}
			<li>
				Disabled more mod{ mods.length > 1 ? "s" : "" }:
				<ul class="list-inside pl-12 text-lg">
					{#each mods as mod}
					<li>{mod}</li>
					{/each}
				</ul>
			</li>
		{/snippet}
		{#snippet entry(html: string)}
			<li>{@html html}</li>
		{/snippet}
		{@render record("Pre-EP2", [
			["two", addedModsWithNote, [[
				"Inventory Profiles Next",
				"Not Enough Animations",
				"Better Than Mending"
			], "Those were previously missed being actually installed but were in the list."]],
			["two", listValues, ["Tried adding mods but unusable for 1.21.11:", ["More Overlays Updated", "oωo"]]],
			["one", addedMods, [
				"libIPN",
				"Fabric Language Kotlin",
				"Untranslated Items"
			]],
			["one", startedDisablingMods, [
				"Compact Help Command",
				"Current Game Music Track",
				"Easy Elevators",
				"Enchanting Commands",
				"Hand Over Your Items",
				"Recipe Commands",
				"Set World Spawn Point",
				"Superflat World No Slimes",
			]]
		])}
		{@render record("Mid-EP2", [
			["one", addedMods, ["Ladders Don't Suck"]]
		])}
	</div>
</div>

<style lang="scss">
    p {
        @apply text-left leading-relaxed;
    }
</style>
