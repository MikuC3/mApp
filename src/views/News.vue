<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>ข่าวสาร</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">ข่าวสาร</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-card>
    <ion-card-header>
      <ion-card-subtitle>ข่าวสาร</ion-card-subtitle>
      <ion-card-title>ข่าวสาร</ion-card-title>
    </ion-card-header>
  </ion-card>

  <ion-card>
    <ion-item>
      <ion-icon :icon="pin" slot="start"></ion-icon>
      <ion-label>ข่าวสาร 1</ion-label>
      <ion-button fill="outline" slot="end">View</ion-button>
    </ion-item>

    <ion-card-content>
      This is content, without any paragraph or header tags,
      within an ion-card-content element.
    </ion-card-content>
  </ion-card>
  
  <ion-card>
    <ion-item>
      <ion-icon :icon="pin" slot="start"></ion-icon>
      <ion-label>ข่าวสาร 2</ion-label>
      <ion-button fill="outline" slot="end">View</ion-button>
    </ion-item>

    <ion-card-content>
      This is content, without any paragraph or header tags,
      within an ion-card-content element.
    </ion-card-content>
  </ion-card>

  <ion-card>
    <ion-item>
      <ion-icon :icon="pin" slot="start"></ion-icon>
      <ion-label>ข่าวสาร 3</ion-label>
      <ion-button fill="outline" slot="end">View</ion-button>
    </ion-item>

    <ion-card-content>
      This is content, without any paragraph or header tags,
      within an ion-card-content element.
    </ion-card-content>
  </ion-card>
      
      <ExploreContainer name="ข่าวสาร" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonIcon, IonItem, IonLabel } from '@ionic/vue';
import { pin } from 'ionicons/icons';
import { defineComponent } from 'vue';

export default defineComponent({
  components: { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonIcon, IonItem, IonLabel },
  setup() {
    return { pin };
  }
})
</script>