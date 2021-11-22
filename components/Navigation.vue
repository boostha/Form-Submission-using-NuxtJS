<template>
  <header class="absolute w-full">
    <nav class="container flex justify-between items-center py-4">
      <div>
        <h1 v-text='navItem.logo' class="font-bold text-2xl"></h1>
      </div>

      <ul class="flex gap-20 text-xl">
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  props: ['navItem']
}
</script>