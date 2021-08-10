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
  <br />
  <ion-list>
       <ion-item-sliding id="item100">
      <ion-item href="#">
        <ion-label>
          <h2>HubStruck Notifications</h2>
          <p>A new message in your network</p>
          <p>Oceanic Next has joined your network</p>
        </ion-label>
        <ion-note slot="end">
          10:45 AM
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="heart"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option color="danger">
          <ion-icon slot="icon-only" :icon="trash"></ion-icon>
        </ion-item-option>
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="star"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

<ion-item-sliding id="item100">
      <ion-item href="#">
        <ion-label>
          <h2>HubStruck Notifications</h2>
          <p>A new message in your network</p>
          <p>Oceanic Next has joined your network</p>
        </ion-label>
        <ion-note slot="end">
          10:45 AM
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="heart"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option color="danger">
          <ion-icon slot="icon-only" :icon="trash"></ion-icon>
        </ion-item-option>
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="star"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
    <ion-item-sliding id="item100">
      <ion-item href="#">
        <ion-label>
          <h2>HubStruck Notifications</h2>
          <p>A new message in your network</p>
          <p>Oceanic Next has joined your network</p>
        </ion-label>
        <ion-note slot="end">
          10:45 AM
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="heart"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option color="danger">
          <ion-icon slot="icon-only" :icon="trash"></ion-icon>
        </ion-item-option>
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="star"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
    <ion-item-sliding id="item100">
      <ion-item href="#">
        <ion-label>
          <h2>HubStruck Notifications</h2>
          <p>A new message in your network</p>
          <p>Oceanic Next has joined your network</p>
        </ion-label>
        <ion-note slot="end">
          10:45 AM
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="heart"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option color="danger">
          <ion-icon slot="icon-only" :icon="trash"></ion-icon>
        </ion-item-option>
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="star"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
    <ion-item-sliding id="item100">
      <ion-item href="#">
        <ion-label>
          <h2>HubStruck Notifications</h2>
          <p>A new message in your network</p>
          <p>Oceanic Next has joined your network</p>
        </ion-label>
        <ion-note slot="end">
          10:45 AM
        </ion-note>
      </ion-item>

      <ion-item-options side="start">
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="heart"></ion-icon>
        </ion-item-option>
      </ion-item-options>

      <ion-item-options side="end">
        <ion-item-option color="danger">
          <ion-icon slot="icon-only" :icon="trash"></ion-icon>
        </ion-item-option>
        <ion-item-option>
          <ion-icon slot="icon-only" :icon="star"></ion-icon>
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
    <!-- Sliding item with text options on both sides -->
    <ion-item-sliding>
      <ion-item-options side="start">
        <ion-item-option @click="favorite(item)">Favorite</ion-item-option>
        <ion-item-option color="danger" @click="share(item)">Share</ion-item-option>
      </ion-item-options>

      <ion-item>
        <ion-label>Item Options</ion-label>
      </ion-item>

      <ion-item-options side="end">
        <ion-item-option @click="unread(item)">Unread</ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

    <!-- Sliding item with expandable options on both sides -->
    <ion-item-sliding>
      <ion-item-options side="start">
        <ion-item-option color="danger" expandable>
          Delete
        </ion-item-option>
      </ion-item-options>

      <ion-item>
        <ion-label>Expandable Options</ion-label>
      </ion-item>

      <ion-item-options side="end">
        <ion-item-option color="tertiary" expandable>
          Archive
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

    <!-- Multi-line sliding item with icon options on both sides -->
 
    <!-- Sliding item with icon start options on end side -->
    <ion-item-sliding>
      <ion-item>
        <ion-label>
          Sliding Item, Icons Start
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option color="primary">
          <ion-icon slot="start" :ios="ellipsisHorizontal" :md="ellipsisVertical"></ion-icon>
          More
        </ion-item-option>
        <ion-item-option color="secondary">
          <ion-icon slot="start" :icon="archive"></ion-icon>
          Archive
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

    <!-- Sliding item with icon end options on end side -->
    <ion-item-sliding>
      <ion-item>
        <ion-label>
          Sliding Item, Icons End
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option color="primary">
          <ion-icon slot="end" :ios="ellipsisHorizontal" :md="ellipsisVertical"></ion-icon>
          More
        </ion-item-option>
        <ion-item-option color="secondary">
          <ion-icon slot="end" :icon="archive"></ion-icon>
          Archive
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

    <!-- Sliding item with icon top options on end side -->
    <ion-item-sliding>
      <ion-item>
        <ion-label>
          Sliding Item, Icons Top
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option color="primary">
          <ion-icon slot="top" :ios="ellipsis-horizontal" :md="ellipsis-vertical"></ion-icon>
          More
        </ion-item-option>
        <ion-item-option color="secondary">
          <ion-icon slot="top" :icon="archive"></ion-icon>
          Archive
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
    

    <!-- Sliding item with icon bottom options on end side -->
    <ion-item-sliding>
      <ion-item>
        <ion-label>
          Sliding Item, Icons Bottom
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option color="primary">
          <ion-icon slot="bottom" :ios="ellipsisHorizontal" :md="ellipsisVertical"></ion-icon>
          More
        </ion-item-option>
        <ion-item-option color="secondary">
          <ion-icon slot="bottom" :icon="archive"></ion-icon>
          Archive
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
     <ion-item-group>
    <ion-item-divider>
      <ion-label>
        Fruits
      </ion-label>
    </ion-item-divider>

    <ion-item-sliding>
      <ion-item>
        <ion-label>
          <h3>Grapes</h3>
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option>
          Favorite
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>

    <ion-item-sliding>
      <ion-item>
        <ion-label>
          <h3>Apples</h3>
        </ion-label>
      </ion-item>
      <ion-item-options>
        <ion-item-option>
          Favorite
        </ion-item-option>
      </ion-item-options>
    </ion-item-sliding>
  </ion-item-group>
  
  </ion-list>
   <ion-list-header>
    <ion-label>List Header</ion-label>
  </ion-list-header>

  <!-- List Header with Button -->
  <ion-list-header>
    <ion-label>New This Week</ion-label>
    <ion-button>See All</ion-button>
  </ion-list-header>

  <!-- List Header with Outline Button -->
  <ion-list-header>
    <ion-label>New This Week</ion-label>
    <ion-button fill="outline">See All</ion-button>
  </ion-list-header>

  <!-- List Header Full Lines -->
  <ion-list-header lines="full">
    <ion-label>New This Week</ion-label>
    <ion-button>See All</ion-button>
  </ion-list-header>

  <!-- List Header Inset Lines -->
  <ion-list-header lines="inset">
    <ion-label>New This Week</ion-label>
    <ion-button>See All</ion-button>
  </ion-list-header>

  <!-- List Headers in Lists -->
  <ion-list>
    <ion-list-header lines="inset">
      <ion-label>Recent</ion-label>
      <ion-button>Clear</ion-button>
    </ion-list-header>
    <ion-item lines="none">
      <ion-label color="primary">
        <h1>I got you babe</h1>
      </ion-label>
    </ion-item>
  </ion-list>

  <ion-list>
    <ion-list-header lines="inset">
      <ion-label>Trending</ion-label>
    </ion-list-header>
    <ion-item>
      <ion-label color="primary">
        <h1>harry styles</h1>
      </ion-label>
    </ion-item>
    <ion-item>
      <ion-label color="primary">
        <h1>christmas</h1>
      </ion-label>
    </ion-item>
    <ion-item lines="none">
      <ion-label color="primary">
        <h1>falling</h1>
      </ion-label>
    </ion-item>
  </ion-list>
</ion-page>

</template>

<script>
import { 
  IonIcon, 
  IonItem, 
  IonItemOption, 
  IonItemOptions, 
  IonItemSliding, 
  IonLabel, 
  IonList,
  IonPage
} from '@ionic/vue';
import { 
  archive, 
  ellipsisHorizontal, 
  ellipsisVertical,
  heart, 
  star, 
  trash
} from 'ionicons/icons';
import { defineComponent } from 'vue';

export default defineComponent({
  components: { 
    IonIcon, 
    IonItem, 
    IonItemOption, 
    IonItemOptions, 
    IonItemSliding, 
    IonLabel, 
    IonList,
    IonPage
  },
  setup() {
    return {
      archive, 
      ellipsisHorizontal, 
      ellipsisVertical,
      heart, 
      star, 
      trash
    }
  }
});
</script>