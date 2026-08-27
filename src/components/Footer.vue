<script setup lang="ts">
import Link from './common/Link.vue'
import { WILDLIGHT_URL } from '@/utils'
</script>

<template>
	<footer>
		<div class="footer-category">
			<h3>Contact</h3>
			<Link :to="WILDLIGHT_URL">GitHub</Link>
			<Link to="https://discord.gg/TcmUQHZ5U4">Discord</Link>
		</div>
		<div class="footer-category">
			<h3>Download</h3>
			<Link to="https://modrinth.com/project/6QzexKXD">Modrinth</Link>
			<Link to="https://www.curseforge.com/minecraft/modpacks/wildlight">CurseForge</Link>
		</div>
	</footer>
</template>
