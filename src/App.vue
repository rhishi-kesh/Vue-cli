<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-7 mt-5">
        <button @click="componentToRender='compHome'">Home</button>
        <button @click="componentToRender='compAbout'">About</button>
        <button @click="componentToRender='compContact'">Contact</button>
        <KeepAlive>
          <component :is="componentToRender"></component>
        </KeepAlive>
      </div>
    </div>
  </div>
</template>

<script>
  import compHome from './Components/compo/Home';
  import compAbout from './Components/compo/About';
  import compContact from './Components/compo/Contact';
  export default {
    data(){
      return {
        componentToRender: "compHome"
      }
    },
    components: {
      compHome,
      compAbout,
      compContact
    }
  }
</script>