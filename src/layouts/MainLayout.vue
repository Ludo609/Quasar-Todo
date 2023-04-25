<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDeaweOpen = !leftDeaweOpen"/>
        </q-toolbar>
        <div class="q-px-lg q-pt-xl q-mb-md">
    <div class="text-h4">Todo_Your Task Manager</div>
       <div class="text-subtitle2">{{todaysDate}}</div>
     </div>
     <q-image src="statics/mountains.jpg" class="header-image absolute-top" />
</q-header>

    <q-drawer
        v-model="leftDeaweOpen"
        show-if-above
        :width="250"
        :breakpoint="600"
      >
        <q-scroll-area style="height: calc(100% - 208px); margin-top: 208px; border-right: 1px solid #ddd">
          <q-list padding>
            <q-item to="/" exact clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="list" />
              </q-item-section>

              <q-item-section>Todo</q-item-section>
            </q-item>
            <q-item to="/help" exact clickable v-ripple>
              <q-item-section avatar>
                <q-icon name="help" />
              </q-item-section>

              <q-item-section>Help</q-item-section>
            </q-item>
             </q-list>
        </q-scroll-area>

        <q-img class="absolute-top" src="https://cdn.quasar.dev/img/material.png" style="height: 208px">
          <div class="absolute-bottom bg-transparent">
            <q-avatar size="55px" class="q-mb-sm">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
            <div class="text-weight-bold">Ludo Uassala</div>
            <div>@Uassala</div>
          </div>
        </q-img>
      </q-drawer>

   <q-page-container>
     <keep-alive>
        <router-view />
      </keep-alive>
    </q-page-container>
  </q-layout>
</template>
