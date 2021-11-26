<template>
<header>
  <Navigation :navItem='siteAssets' />
  <Hero :heroItem='siteAssets'/>
  <Section />
  <Footer :foot='siteAssets'/>
</header>
</template>

<script>
export default {
  data() {
    return {
      siteAssets: {
          logo: 'CPNT200',
          hero: 'Ideas for this website',
          footer: '<p>&copy; David Ha</p>',
      }
    }
  }
}
</script>
