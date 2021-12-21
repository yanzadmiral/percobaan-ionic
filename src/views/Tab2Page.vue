<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Photo Gallery</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-content>
        <ion-grid>
          <ion-row>
            <ion-col size="6" :key="photo" v-for="photo in photos">
              <ion-img :src="photo.webviewPath"></ion-img>
            </ion-col>
          </ion-row>
        </ion-grid>

        <ion-fab vertical="bottom" horizontal="center" name="fixed">
        <ion-fab-button @click="takePhoto()">
          <ion-icon :icon="camera"></ion-icon>
        </ion-fab-button>
      </ion-fab>
      </ion-content>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { camera, trash, close } from "ionicons/icons";
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
} from "@ionic/vue";
import { usePhotoGallery } from "@/composables/usePhotoGallery";

export default {
  name: "Tab-2",
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
  },
  setup() {
    const { photos,takePhoto } = usePhotoGallery();

    return {
      photos,
      takePhoto,
      camera,
      trash,
      close,
    };
  },
};
</script>
