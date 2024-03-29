<template>
  <v-layout>
    <v-navigation-drawer
        v-model="drawer"
        temporary
        theme="dark"
        class=""
    >
      <v-list>
        <v-list-item class="rounded-xl rounded-be-0" style="background-color: red">first</v-list-item>
        <v-list-item>second</v-list-item>
        <v-list-item>third</v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar>
      <v-app-bar-title>Application Bar</v-app-bar-title>
      <v-btn
        @click.stop="drawer = !drawer"
        class="menu-toggler"
      >
        Toggle
      </v-btn>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-layout>
</template>

<script setup lang="ts">
import {ref} from "vue";

const drawer = ref<boolean>(false);
</script>
