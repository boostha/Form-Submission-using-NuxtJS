<template>
  <footer class='bg-gray-500'>
    <div class="container flex justify-between items-center h-20 text-white">
      <div v-html="foot.footer"></div>
      <ul>
        <li>About</li>
        <li>Contact</li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  props:['foot']
}
</script>