<script setup lang="ts">
import WikiNav from '../../components/WikiNav.vue'
import Link from '@/components/common/Link.vue'
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
				<Link to="https://github.com/Novalight-Studios/WildLight-Compat">
					WildLight Compat
				</Link>
				adds some compatibility fixes between:
			</p>
			<ul>
				<li>
					<Link to="https://modrinth.com/project/idGcORfw">Detail Armor Bar Compat</Link>
					and
					<Link to="https://modrinth.com/project/eE2Db4YU">Immersive Armors</Link>: the
					armors were not compatible. Waiting for
					<Link to="https://github.com/Raik176/detail-armor-bar-compat/pull/19">
						PR #19 </Link
					>.
				</li>
				<li>
					<Link to="https://modrinth.com/project/idGcORfw">Detail Armor Bar Compat</Link>
					and <Link to="https://modrinth.com/project/a1llHwl4">Copper Age Backport</Link>:
					the armors were not compatible.
				</li>

				<li>
					<Link to="https://modrinth.com/project/YQnwl5Vv">Visual Overhaul</Link>
					and all modded woods: the wood in the furnace wasn't textured. Waiting for
					<Link to="https://github.com/TeamMidnightDust/VisualOverhaul/pull/99"
						>POUR #99</Link
					>.
				</li>
				<li>
					<Link to="https://modrinth.com/project/4q8UOK1d">Subtle Effects</Link>
					and
					<Link to="https://modrinth.com/project/a1llHwl4">Copper Age Backport</Link>:
					wrong particles on lights
				</li>
				<li>
					<Link to="https://modrinth.com/project/4q8UOK1d">Subtle Effects</Link> and
					<Link to="https://modrinth.com/project/fnAffV0n">Deeper and Darker</Link>:
					Sludge trail particles
				</li>
				<li>
					<Link to="https://modrinth.com/project/4q8UOK1d">Subtle Effects</Link> and
					<Link to="https://modrinth.com/project/XHXMTS5X">Soul Candles</Link>: particles
					on candles
				</li>
				<li>
					<Link to="https://modrinth.com/project/nvQzSEkH">Jade</Link> and
					<Link to="https://modrinth.com/project/U5SedJ9S">Enhanced Boss Bar</Link>:
					tooltips behind the boss bar
				</li>
				<li>
					<Link to="https://modrinth.com/project/S2guHrs2">Fancy Block Particles</Link>
					and <Link to="https://modrinth.com/project/dspVZXKP">Fast Better Grass</Link>:
					gray particles when breaking a block
				</li>
				<li>
					<Link to="https://modrinth.com/project/U5SedJ9S">Enhanced Boss Bar</Link>: with
					multiple bosses: add more spaces between boss bars
				</li>
				<li>
					<Link to="https://modrinth.com/project/a1llHwl4">Copper Age Backport</Link>:
					remove the End Flashes backported
				</li>
				<li>
					<Link to="https://modrinth.com/project/VLAWWg1B">useful Backpack</Link>: Allows
					you to close the backpack screen with the backpack keybind (V by default)
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
