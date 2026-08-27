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
			<h1>How to install WildLight</h1>
			<p>
				You can install the WildLight modpack using either
				<Link to="https://modrinth.com/project/6QzexKXD">Modrinth</Link> or
				<Link to="https://www.curseforge.com/minecraft/modpacks/wildlight">CurseForge</Link
				>. Simply visit the project page on your preferred platform, click the installation
				button (or download the modpack file for manual import), and launch it through your
				chosen Minecraft launcher. Both methods work the same way, and installation is quick
				and straightforward!
			</p>
			<p>
				<strong>Need help?</strong> If you have trouble installing, check the documentation
				on Modrinth/CurseForge or ask for help on the
				<Link to="https://discord.gg/TcmUQHZ5U4">WildLight Discord server </Link>.
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
