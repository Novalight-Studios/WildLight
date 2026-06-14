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
          and <a href="https://modrinth.com/project/eE2Db4YU" target="_blank">Immersive Armors</a>:
          the armors were not compatible. Waiting for
          <a href="https://github.com/Raik176/detail-armor-bar-compat/pull/19" target="_blank"
            >pull request #19</a
          >.
        </li>
        <li>
          <a href="https://modrinth.com/project/idGcORfw" target="_blank"
            >Detail Armor Bar Compat</a
          >
          and
          <a href="https://modrinth.com/project/a1llHwl4" target="_blank">Copper Age Backport</a>:
          the armors were not compatible.
        </li>

        <li>
          <a href="https://modrinth.com/project/YQnwl5Vv" target="_blank">Visual Overhaul</a> and
          all modded woods: the wood in the furnace wasn't textured. Waiting for
          <a href="https://github.com/TeamMidnightDust/VisualOverhaul/pull/99" target="_blank"
            >pull request #99</a
          >.
        </li>
        <li>
          <a href="https://modrinth.com/project/VLAWWg1B" target="_blank">Useful Backpack</a>:
          Allows you to close the backpack screen with the backpack keybind (V by default)
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
