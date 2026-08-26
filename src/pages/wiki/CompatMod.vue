<script setup lang="ts">
import WikiNav from '../../components/WikiNav.vue'
import { onMounted } from 'vue'

onMounted(() => {
	const nav = document.querySelector('nav')
	const main = document.querySelector('main')
	if (nav && main) {
		main.style.paddingTop = nav.offsetHeight + 'px'
	}
})
</script>

<template>
	<main>
		<WikiNav />
		<section class="wiki-content">
			<h1>Mods compatibility</h1>
			<p>
				<a href="https://github.com/Novalight-Studios/WildLight-Compat" target="_blank"
					>WildLight Compat</a
				>
				adds some compatibility fixes between:
			</p>
			<ul>
				<li>
					<a href="https://modrinth.com/project/idGcORfw" target="_blank"
						>Detail Armor Bar Compat</a
					>
					and
					<a href="https://modrinth.com/project/eE2Db4YU" target="_blank"
						>Immersive Armors</a
					>: the armors were not compatible. Waiting for
					<a
						href="https://github.com/Raik176/detail-armor-bar-compat/pull/19"
						target="_blank"
						>pull request #19</a
					>.
				</li>
				<li>
					<a href="https://modrinth.com/project/idGcORfw" target="_blank"
						>Detail Armor Bar Compat</a
					>
					and
					<a href="https://modrinth.com/project/a1llHwl4" target="_blank"
						>Copper Age Backport</a
					>: the armors were not compatible.
				</li>

				<li>
					<a href="https://modrinth.com/project/YQnwl5Vv" target="_blank"
						>Visual Overhaul</a
					>
					and all modded woods: the wood in the furnace wasn't textured. Waiting for
					<a
						href="https://github.com/TeamMidnightDust/VisualOverhaul/pull/99"
						target="_blank"
						>pull request #99</a
					>.
				</li>
				<li>
					<a href="https://modrinth.com/project/4q8UOK1d" target="_blank"
						>Subtle Effects</a
					>
					and
					<a href="https://modrinth.com/project/a1llHwl4" target="_blank"
						>Copper Age Backport</a
					>: wrong particles on lights
				</li>
				<li>
					<a href="https://modrinth.com/project/4q8UOK1d" target="_blank"
						>Subtle Effects</a
					>
					and
					<a href="https://modrinth.com/project/fnAffV0n" target="_blank"
						>Deeper and Darker</a
					>: Sludge trail particles
				</li>
				<li>
					<a href="https://modrinth.com/project/4q8UOK1d" target="_blank"
						>Subtle Effects</a
					>
					and
					<a href="https://modrinth.com/project/XHXMTS5X" target="_blank">Soul Candles</a
					>: particles on candles
				</li>
				<li>
					<a href="https://modrinth.com/project/nvQzSEkH" target="_blank">Jade</a> and
					<a href="https://modrinth.com/project/U5SedJ9S" target="_blank"
						>Enhanced Boss Bar</a
					>: tooltips behind the boss bar
				</li>
				<li>
					<a href="https://modrinth.com/project/S2guHrs2" target="_blank"
						>Fancy Block Particles</a
					>
					and
					<a href="https://modrinth.com/project/dspVZXKP" target="_blank"
						>Fast Better Grass</a
					>: gray particles when breaking a block
				</li>
				<li>
					<a href="https://modrinth.com/project/U5SedJ9S" target="_blank"
						>Enhanced Boss Bar</a
					>
					with multiple bosses: add more spaces between boss bars
				</li>
				<li>
					<a href="https://modrinth.com/project/a1llHwl4" target="_blank"
						>Copper Age Backport</a
					>: remove the End Flashes backported
				</li>
				<li>
					<a href="https://modrinth.com/project/VLAWWg1B" target="_blank"
						>Useful Backpack</a
					>: Allows you to close the backpack screen with the backpack keybind (V by
					default)
				</li>
			</ul>
		</section>
	</main>
</template>

<style scoped>
main {
	flex-direction: row;
	align-items: flex-start;
	width: 100vw;
	max-width: 100vw;
	box-sizing: border-box;
}

@media (max-width: 1024px) {
	main {
		flex-direction: column;
	}
}
</style>
