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
      <h1>Credits</h1>
      <ul>
        <li>
          Thanks to <a href="https://github.com/nNoidea" target="_blank">nNoidea</a> for Eating
          Animation support for Wilder Wild compatibility! (via
          <a href="https://github.com/Theoness1/EatingAnimation/pull/62" target="_blank"
            >Eating Animation PR #62</a
          >)
          <br />
          Note: this compaibility is not anymore in this mod, but in this
          <a href="https://github.com/Alfakynz/Eating-Animation-Modded" target="_blank"
            >resource pack</a
          >
        </li>
        <li>
          Thanks to the
          <a href="https://modrinth.com/organization/tuit06dH" target="_blank">FrozenBlock team</a>
          for <a href="https://modrinth.com/project/AtHRJSUW" target="_blank">WilderWild</a>, and to
          <a href="https://modrinth.com/user/GgcBbYdM" target="_blank">voxelotl</a> for allowing me
          to add some of their textures to the resource pack!
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
