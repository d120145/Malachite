<script lang="tsx">
import FooterVue from '~~/components/Footer.vue';
import HeaderVue from '~~/components/Header.vue';
import HomeGithubLinkContentVue from '~~/components/HomeGithubLinkContent.vue';
import HomeListContentVue from '~~/components/HomeListContent.vue';
import HomeTopContentVue from '~~/components/HomeTopContent.vue';
import MainVue from '~~/components/templates/Main.vue';

export default defineComponent({

setup(){
  useSeoMeta({
    title: 'Hello Nuxt',
  })
},

render(){
  return (
    <>
    <HeaderVue />
    <MainVue>
      <HomeTopContentVue />
      <HomeListContentVue />
      <HomeGithubLinkContentVue />
    </MainVue>
    <FooterVue />
    </>
  )
  }
})
</script>
