<template>
  <DashboardNav />
  <router-view />
  <FooterBar />
</template>
<script>
import DashboardNav from "@/components/TopNav.vue";
import FooterBar from "@/components/FooterBar.vue";
export default {
  name: "App",
  components: {
    DashboardNav,
    FooterBar
  },
  computed: {
    // hide() {
    //   const hiddenPages = [
    //     'LoginPage', 'RegistrationPage', 'EmailVerificationPage', 'ForgotPasswordPage', 'ResetPasswordPage',
    //     'BasicDetails', 'ConnectDetails', 'OverviewDetails', 'WorktimeDetails', 'BusinessTypeDetails', 'BrandingDetails',
    //     'ProductList', 'CreateProduct', 'CollectionList', 'RewardsDetails', 'DashboardPage', 'ReviewListPage', 'SupportersDetails', 'FamesetDetails', 'CategoryDetails', 'BankDetails', 'SocialDetails'
    //   ]
    //   return hiddenPages.includes(this.$route.name)
    // }, 
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
