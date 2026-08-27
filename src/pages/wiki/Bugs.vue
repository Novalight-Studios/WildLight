<script setup lang="ts">
import WikiNav from '../../components/WikiNav.vue'
import Link from '@/components/common/Link.vue'
import { onMounted } from 'vue'
import { WILDLIGHT_URL } from '@/utils/index.ts'

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
			<h1>How to report a bug or suggest an idea</h1>
			<p>
				If you encounter a bug in WildLight, have an idea to suggest, or want me to create a
				standalone mod or resource pack that's separate from WildLight Compat, please let me
				know! You can use either of the following methods:
			</p>
			<ol>
				<li>
					<strong> Open an issue on <Link :to="WILDLIGHT_URL">GitHub</Link> </strong>
					<ul>
						<li>Go to my <Link :to="WILDLIGHT_URL">GitHub Issues page</Link>.</li>
						<li>
							Click on <strong>New issue</strong> and fill out the template with as
							much detail as possible (for bugs: steps to reproduce, expected
							behavior, screenshots, etc.; for ideas: describe your suggestion and why
							you think it would help).
						</li>
						<li>
							Submit the issue. I track and respond to bugs and ideas here regularly.
						</li>
					</ul>
				</li>
				<li>
					<strong>
						Post a bug or idea on my
						<Link to="https://discord.gg/TcmUQHZ5U4">Discord server</Link>:
					</strong>
					<ul>
						<li>
							Join the
							<Link to="https://discord.gg/TcmUQHZ5U4">WildLight Discord</Link>.
						</li>
						<li>
							For bugs, post in the <strong>#bugs</strong> channel.<br />
							For ideas or suggestions, post in the
							<strong>#suggestions-and-ideas</strong> channel.
						</li>
						<li>
							Describe your bug or idea clearly, including steps to reproduce and any
							relevant screenshots or logs for bugs, or details and reasoning for
							ideas.
						</li>
					</ul>
				</li>
			</ol>
			<p>Thank you for helping me improve WildLight!</p>
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
