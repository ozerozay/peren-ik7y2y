<template>
  <ion-page>
    <ion-toolbar>
    <ion-buttons slot="start">
      <ion-menu-button auto-hide="false"></ion-menu-button>

    </ion-buttons>
    <ion-buttons slot="secondary">
      <ion-button>
        <ion-icon slot="icon-only" :icon="star"></ion-icon>
      </ion-button>
    </ion-buttons>
     <ion-buttons slot="end">
     <ion-button>
        <ion-icon slot="icon-only" :icon="star"></ion-icon>
      </ion-button>
    </ion-buttons>
    <ion-title>Talepler</ion-title>
  </ion-toolbar>
    <ion-content class="ion-padding">
       <ion-grid>
    <ion-row>
      <ion-col size="9">
        <ion-searchbar placeholder="Ara..." show-cancel-button="never"></ion-searchbar>
      </ion-col>
      <ion-col size="12">
         <ion-select multiple="true" placeholder="Seç" cancel-text="İptal" ok-text="Seç">
        <ion-select-option value="Bekleniyor">Bekleniyor</ion-select-option>
        <ion-select-option value="olives">Cevapsız</ion-select-option>
        <ion-select-option value="xcheese">Sonra Ara</ion-select-option>
        <ion-select-option value="peppers">İlgilenmiyor</ion-select-option>
        <ion-select-option value="mushrooms">Mesafe Uzak</ion-select-option>
        <ion-select-option value="onions">Kendisi Arayacak</ion-select-option>
        <ion-select-option value="pepperoni">Meşgul</ion-select-option>
        <ion-select-option value="pineapple">Pahalı</ion-select-option>
        <ion-select-option value="sausage">Yanlış Numara</ion-select-option>
        <ion-select-option value="Spinach">Randevu İptal</ion-select-option>
      </ion-select>
      </ion-col>
    </ion-row>
       </ion-grid>

      <ion-button @click="toggleInfiniteScroll" v-if="1==2" expand="block">
        Toggle Infinite Scroll
      </ion-button>

      <ion-list>
        <ion-item-sliding id="item100" v-for="item in items" :key="item">
      <ion-item href="#">
        <ion-label>
          <h2>Cihat Özer Özay</h2>
          <p>Aranmak istemiyor / Melike</p>
          <p>0 / 3 Randevu</p>
          <p><b>Son İşlem: 20.08.2021</b></p>
        </ion-label>
        <ion-note slot="end">
          CEVAPSIZ
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="call"></ion-icon>
        </ion-item-option>
        <ion-item-option color="success">
          <ion-icon slot="icon-only" :icon="logoWhatsapp"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="add"></ion-icon>
        </ion-item-option>
        <ion-item-option color="success">
          <ion-icon slot="icon-only" :icon="calendar"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
        <ion-item >
          <ion-label>{{ item }}</ion-label>
        </ion-item>
      </ion-list>

      <ion-infinite-scroll
        @ionInfinite="loadData($event)" 
        threshold="100px" 
        id="infinite-scroll"
        :disabled="isDisabled"
      >
        <ion-infinite-scroll-content
          loading-spinner="bubbles"
          loading-text="Yükleniyor...">
        </ion-infinite-scroll-content>
      </ion-infinite-scroll>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { 
  IonButton,
  IonContent, 
  IonInfiniteScroll, 
  IonInfiniteScrollContent,
  IonItem,
  IonLabel,
  IonList,
  IonRow,
  IonCol,
  IonPage,
  IonSelect,
  IonSelectOption
 } from '@ionic/vue';
 import { 
  archive, 
  ellipsisHorizontal, 
  ellipsisVertical,
  heart, 
  star, 
  trash,
  calendar,
  add,
  call,
  logoWhatsapp
} from 'ionicons/icons';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  components: {
    IonButton,
    IonContent, 
    IonInfiniteScroll, 
    IonInfiniteScrollContent,
    IonItem,
    IonLabel,
    IonList,
    IonPage,
    IonRow,
    IonCol,
    IonSelect,
    IonSelectOption
  },
  setup() {
    const isDisabled = ref(false);
    const toggleInfiniteScroll = () => {
      isDisabled.value = !isDisabled.value;
    }
    const items = ref([]);
    const pushData = () => {
      const max = items.value.length + 20;
      const min = max - 20;
      for (let i = min; i < max; i++) {
        // eslint-disable-next-line @typescript-eslint/ban-ts-ignore
      //@ts-ignore
        items.value.push(i);
      }
    }

    const loadData = (ev: CustomEvent) => {
      setTimeout(() => {
        pushData();
        console.log('Loaded data');
        // eslint-disable-next-line @typescript-eslint/ban-ts-ignore
      //@ts-ignore
        ev.target.complete();

        // App logic to determine if all data is loaded
        // and disable the infinite scroll
        if (items.value.length == 1000) {
          // eslint-disable-next-line @typescript-eslint/ban-ts-ignore
      //@ts-ignore
          ev.target.disabled = true;
        }
      }, 500);
    }

    pushData();

    return {
      isDisabled,
      toggleInfiniteScroll,
      loadData,
      items,
       archive, 
      ellipsisHorizontal, 
      ellipsisVertical,
      heart, 
      star, 
      trash,
      calendar,
      add,
      call,
      logoWhatsapp
    }
  }
});

</script>