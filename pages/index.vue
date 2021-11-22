<template>
<header>
  <Navigation :navItem='siteAssets' />
  <Hero :heroItem='siteAssets'/>
  <Footer :foot='siteAssets'/>
</header>
</template>

<script>
export default {
  data() {
    return {
      siteAssets: {
          logo: 'CPNT200',
          hero: 'Create Something Amazing',
          footer: '<p>&copy; David Ha</p>',
      }
    }
  }
}
</script>
