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
			<h1>Credits</h1>
			<ul>
				<li>
					Thanks to <Link to="https://github.com/nNoidea">nNoidea</Link> for Eating
					Animation support for Wilder Wild compatibility! (via
					<Link to="https://github.com/Theoness1/EatingAnimation/pull/62">
						Eating Animation PR #62 </Link
					>)
					<br />
					Note: this compaibility is not anymore in this mod, but in this
					<Link
						to="https://github.com/Novalight-Studios/Eating-Animation-Modded"
						target="_blank"
						>resource pack</Link
					>
				</li>
				<li>
					Thanks to the
					<Link to="https://modrinth.com/organization/tuit06dH">FrozenBlock team</Link>
					for
					<Link to="https://modrinth.com/project/AtHRJSUW">WilderWild</Link>, and to
					<Link to="https://modrinth.com/user/GgcBbYdM">voxelotl</Link> for allowing me to
					add some of their textures to the resource pack!
				</li>
				<li>Thanks to Annie for making the beautiful WildLight logo</li>
			</ul>
			<p>
				And a big thanks as well to every other mod, resource pack, and shader creator! Your
				projects are all awesome!
			</p>
		</section>
	</main>
</template>

<style scoped>
main {
	display: flex;
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
