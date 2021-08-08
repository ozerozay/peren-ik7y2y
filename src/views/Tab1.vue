<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-context v-if="state.loading">
      <div class="loading-center">
        <ion-spinner color="primary"></ion-spinner>
      </div>
    </ion-context>

    <ion-content v-else :fullscreen="true">
      <ion-refresher slot="fixed" @ionRefresh="doRefresh">
        <ion-refresher-content></ion-refresher-content>
      </ion-refresher>
      <ion-card>
        <ion-card-header>
          <img :src="state.randomCoctail.strDrinkThumb" />
          <ion-card-subtitle>
            {{ state.randomCoctail.strCategory }} | Served In
            {{ state.randomCoctail.strGlass }}
          </ion-card-subtitle>
          <ion-card-title>
            {{ state.randomCoctail.strDrink }}
          </ion-card-title>
          <ion-card-content>
            <p>{{ state.randomCoctail.strInstructions }}</p>
            <ion-list-header>
              <ion-list>
                <ion-item v-if="state.randomCoctail.strIngredient1">
                  <ion-label>
                    <span v-if="state.randomCoctail.strMeasure1">
                      {{ state.randomCoctail.strMeasure1 }} -
                    </span>
                    {{ state.randomCoctail.strIngredient1 }}
                  </ion-label>
                </ion-item>
                <ion-item v-if="state.randomCoctail.strIngredient2">
                  <ion-label>
                    <span v-if="state.randomCoctail.strMeasure2">
                      {{ state.randomCoctail.strMeasure2 }} -
                    </span>
                    {{ state.randomCoctail.strIngredient2 }}
                  </ion-label>
                </ion-item>
              </ion-list>
            </ion-list-header>
          </ion-card-content>
        </ion-card-header>
      </ion-card>

      <ion-header v-if="1 == 2" collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue";
import ExploreContainer from "@/components/ExploreContainer.vue";
import { reactive } from "vue";
import axios from "axios";

export default {
  name: "Tab1",
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
  },
  setup() {
    const state = reactive({
      randomCoctail: {},
      loading: false,
    });

    const fetchRandomCoctail = async (dispLoaderPage: boolean) => {
      if (dispLoaderPage) {
        state.loading = true;
      }

      const res = await axios.get(
        "https://www.thecocktaildb.com/api/json/v1/1/random.php"
      );

      if (res.data) {
        state.randomCoctail = res.data.drinks[0];
      }

      state.loading = false;
    };

    const doRefresh = (event: CustomEvent) => {
      fetchRandomCoctail(false);

      // eslint-disable-next-line @typescript-eslint/ban-ts-ignore
      //@ts-ignore
      event.target.complete();
    };

    fetchRandomCoctail(true);

    return {
      state,
      fetchRandomCoctail,
      doRefresh,
    };
  },
};
</script>

<style>
.loading-center {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 90vh;
}

ion-spinner {
  transform: scale(1.5);
}
</style>