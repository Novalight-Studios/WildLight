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
			<h1>Tools</h1>
			<p>
				To develop WildLight, I relied on a set of tools that helped keep the project
				organized, scalable, and easy to maintain.
			</p>
			<p>
				First, <Link to="https://github.com">GitHub</Link> served as the backbone of the
				project, allowing me to store the code, track changes over time, and keep a clean
				development history.
			</p>
			<p>
				For managing the mods, I used
				<Link to="https://packwiz.infra.link">Packwiz</Link>, an essential tool that lets me
				add, update, or remove mods without placing JAR files directly inside the modpack
				folder. This makes the project lighter, more modular, and far more maintainable.
			</p>
			<p>
				Since I needed to maintain two versions (CurseForge and Modrinth) of the modpack
				across different directories, I created
				<Link to="https://github.com/Alfakynz/PackWize">PackWize</Link>. Instead of running
				Packwiz commands separately in each subdirectory, one for Modrinth, another for
				CurseForge, and so on, PackWize allows me to run a single command at the project
				root that automatically executes the required Packwiz actions everywhere. This
				drastically simplifies the workflow and prevents repetitive manual steps.
			</p>
			<p>
				For editing configuration files, organizing the project structure, and managing all
				the technical details, I worked with
				<Link to="https://code.visualstudio.com">Visual Studio Code</Link> as my IDE. Its
				integrated terminal let me execute Packwiz and PackWize commands directly, making
				the workflow smooth and efficient.
			</p>
			<p>
				Finally, to test WildLight in different environments, I used two launchers:
				<Link to="https://www.curseforge.com">CurseForge</Link> and
				<Link to="https://modrinth.com">Modrinth</Link>. Testing on both ensured optimal
				compatibility and made sure the modpack installs easily no matter which launcher
				players prefer.
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
