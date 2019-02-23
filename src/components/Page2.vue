<template>
  <ion-app>
    <ion-page class="show-page">
      
      <ion-header>
        <ion-toolbar>
          <ion-title>Ionic 4 + Vue Application </ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-content class="content" padding>
        This is page 2
        
        <ion-button @click="goToHome" full>Go Home</ion-button>

         <button v-on:click="getDeviceInfo()">Get Device Data</button>
         <p> {{ info }}</p> 

      </ion-content>
    </ion-page>
  </ion-app>
</template>

<script>
import { Plugins } from "@capacitor/core";
const { Device } = Plugins;

export default {
  name: 'Page2',
  data () {
    return {
      info: null
    }
  },  
  methods: {
      goToHome(){
          this.$router.push('/')
      },
      async getDeviceInfo() {
        this.info = await Device.getInfo();
      }
  }  
}
</script>

<style>

</style>


