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
			<h1>Resource Packs compatibility</h1>
			<p>
				<Link to="https://github.com/Novalight-Studios/WildLight-Compat">
					WildLight Compat
				</Link>
				adds some compatibility fixes between:
			</p>
			<ul>
				<li>
					<Link to="https://modrinth.com/project/sQCUH0Mr">
						Recolourful Containers GUI + HUD (DARK)
					</Link>
					with:
					<ul>
						<li>
							<Link to="https://modrinth.com/project/bRFWnJ87">
								Animal Feeding Trough
							</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/IhBYAM6m">
								Enhanced Workbenches
							</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/4I1XuqiY">
								Entity Model Features
							</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/mOgUt4GM">Mod Menu</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/j7Ux0G0U">Not Interested!</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/tagwiZkJ">Polymorph</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/VLAWWg1B">Useful Backpacks</Link>
						</li>
					</ul>
				</li>
				<li>
					<Link to="https://modrinth.com/project/O7z3QKAG">Icons</Link> with:
					<ul>
						<li>
							<Link to="https://modrinth.com/project/mOgUt4GM">Mod Menu</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/DnyS3EEW">Options Profiles</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/AANobbMI">Sodium</Link>
						</li>
						<li>
							<Link to="https://modrinth.com/project/ZouiUX7t">Sounds</Link>
						</li>
					</ul>
				</li>
				<li>
					<Link to="https://modrinth.com/project/6xwxDTgf">Vanilla Backport</Link>
					with:
					<ul>
						<li>
							<Link to="https://modrinth.com/project/AtHRJSUW">Wilder Wild</Link>
							(spawn eggs from newer versions)
						</li>
					</ul>
				</li>
				<li>
					<Link to="https://modrinth.com/project/8AX2hHnX">Simple Music Control</Link>
					with:
					<ul>
						<li>
							<Link to="https://modrinth.com/project/AtHRJSUW">Wilder Wild</Link>
							(music names)
						</li>
						<li>
							<Link to="https://modrinth.com/project/6xwxDTgf">Vanilla Backport</Link>
							(music names)
						</li>
					</ul>
				</li>
				<li>
					<Link to="https://modrinth.com/project/3MCobCxw">Better Lights</Link>: a bug
					with chains
				</li>
				<li>
					<Link to="https://modrinth.com/project/nvQzSEkH">Jade</Link>: some animals
					didn't have a name
				</li>
				<li>
					<Link to="https://modrinth.com/project/dWloHgVp">CIT Painting Icons</Link>: icon
					for Dennis variant
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
