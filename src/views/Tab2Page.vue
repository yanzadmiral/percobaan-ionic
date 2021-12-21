<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Photo Gallery</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>
      
      <ExploreContainer name="Tab 2 page" />
    </ion-content>
    <ion-content :fullscreen="true">
  <ion-fab vertical="bottom" horizontal="center" slot="fixed">
    <ion-fab-button @click="takePhoto()">
      <ion-icon :icon="camera"></ion-icon>
    </ion-fab-button>
  </ion-fab>
</ion-content>
  </ion-page>
</template>

<script lang="ts">
import { camera, trash, close } from 'ionicons/icons';
import {
  IonPage,
  IonHeader,
  IonFab,
  IonFabButton,
  IonIcon,
  IonToolbar,
  IonTitle,
  IonContent,
  IonGrid,
  IonRow,
  IonCol,
  IonImg,
} from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

export default  {
  name: 'Tab-2',
  components: {
    IonPage,
    IonHeader,
    // eslint-disable-next-line vue/no-unused-components
    IonFab,
    // eslint-disable-next-line vue/no-unused-components
    IonFabButton,
    // eslint-disable-next-line vue/no-unused-components
    IonIcon,
    IonToolbar,
    IonTitle,
    IonContent,
    // eslint-disable-next-line vue/no-unused-components
    IonGrid,
    // eslint-disable-next-line vue/no-unused-components
    IonRow,
    // eslint-disable-next-line vue/no-unused-components
    IonCol,
    // eslint-disable-next-line vue/no-unused-components
    IonImg,
    ExploreContainer
  },
  setup() {
    return {
      camera,
      trash,
      close,
    };
  },
}
</script>