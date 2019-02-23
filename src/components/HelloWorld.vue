<template>
    <ion-page class="show-page">

      <!-- <ion-header>
        <ion-toolbar>
          <ion-title>Ionic 4 + Vue Application </ion-title>
        </ion-toolbar>
      </ion-header> -->
      
      <ion-content class="content" padding>
        <!-- fab placed to the top end -->
        <ion-fab vertical="top" horizontal="end" slot="fixed">
          <ion-fab-button>
            <ion-icon name="add"></ion-icon>
          </ion-fab-button>
        </ion-fab>
        <ion-card>
          <ion-card-header>
            <ion-card-subtitle>Card Subtitle</ion-card-subtitle>
            <ion-card-title>Card Title</ion-card-title>
          </ion-card-header>

          <ion-card-content>
            Keep close to Nature's heart... and break clear away, once in awhile,
            and climb a mountain or spend a week in the woods. Wash your spirit clean.
          </ion-card-content>
        </ion-card>

        <ion-card>
          <ion-item>
            <ion-icon name="pin" slot="start"></ion-icon>
            <ion-label>ion-item in a card, icon left, button right</ion-label>
            <ion-button fill="outline" slot="end">View</ion-button>
          </ion-item>

          <ion-card-content>
            This is content, without any paragraph or header tags,
            within an ion-card-content element.
          </ion-card-content>
        </ion-card>

          <ion-list>
            <ion-item>
              <ion-label>Pokémon Yellow</ion-label>
            </ion-item>
            <ion-item>
              <ion-label>Mega Man X</ion-label>
            </ion-item>
            <ion-item>
              <ion-label>The Legend of Zelda</ion-label>
            </ion-item>
            <ion-item>
              <ion-label>Pac-Man</ion-label>
            </ion-item>
            <ion-item>
              <ion-label>Super Mario World</ion-label>
            </ion-item>
          </ion-list>

           <ion-button @click="goToPage2" full>Go To Page II</ion-button>
      </ion-content>

    </ion-page>
</template>

<script>
export default {
  name: 'HelloWord',
  data () {
    return {
      items: [{id: 0, name: 'Ahmed'}, {id: 1, name: 'Naima'}]
    }
  },  
  methods: {
    goToPage2 () {
      this.$router.push('page2')
    }
  }  
}
</script>
