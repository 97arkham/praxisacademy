<template>
  <div>
    <v-card class="mx-auto overflow-hidden">
      <!-- dekstop -->
      <v-app-bar color="#0b55d3" height="80px" dark fixed elevate-on-scroll>
        <router-link to="/" class="text-decoration-none">
          <v-toolbar-title>
            <v-img :src="logo" width="50" />
          </v-toolbar-title>
        </router-link>

        <v-spacer></v-spacer>

        <div class="mr-5 hidden-xs-only">
          <v-menu left bottom>
            <template v-slot:activator="{ on, attrs }">
              <div v-bind="attrs" v-on="on">
                <span>Program</span>
              </div>
            </template>

            <v-list>
              <router-link
                to="/program/fullstack-developer"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title>Fullstack developer</v-list-item-title>
                </v-list-item>
              </router-link>

              <router-link
                to="/program/python-developer"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title>Python developer</v-list-item-title>
                </v-list-item>
              </router-link>

              <router-link
                to="/program/frontend-developer"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title>Frontend developer</v-list-item-title>
                </v-list-item>
              </router-link>

              <router-link
                to="/program/mobile-developer"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title>Mobile developer</v-list-item-title>
                </v-list-item>
              </router-link>

              <router-link
                to="/program/nodejs-programming"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title>Nodejs programming</v-list-item-title>
                </v-list-item>
              </router-link>
            </v-list>
          </v-menu>
        </div>

        <div class="mr-5 hidden-xs-only">
          <router-link to="/creation" class="text-decoration-none">
            <span class="white--text">Karya</span>
          </router-link>
        </div>

        <!-- <div class="mr-5 hidden-xs-only">
          <router-link to="/activity" class="text-decoration-none">
            <span class="white--text">Kegiatan</span>
          </router-link>
        </div>` -->

        <div class="mr-5 hidden-xs-only">
          <router-link to="/register/syarat" class="text-decoration-none">
            <span class="white--text">Bootcamp</span>
          </router-link>
        </div>

        <v-app-bar-nav-icon
          class="hidden-sm-and-up"
          @click="sideNav = true"
        ></v-app-bar-nav-icon>
      </v-app-bar>

      <!-- mobile -->
      <v-navigation-drawer v-model="sideNav" right fixed temporary>
        <v-list-item>
          <v-list-item-content>
            <v-list-item-avatar>
              <img :src="logo" />
            </v-list-item-avatar>
          </v-list-item-content>

          <v-list-item-content>
            <v-list-item-title>Praxis</v-list-item-title>
            <v-list-item-subtitle>academy</v-list-item-subtitle>
          </v-list-item-content>

          <v-spacer></v-spacer>

          <v-app-bar-nav-icon class="hidden-sm-and-up" @click="sideNav = false">
            <v-icon>mdi-window-close</v-icon>
          </v-app-bar-nav-icon>
        </v-list-item>

        <v-divider></v-divider>
        <!-- coba -->
        <v-list-group
        :value="false"
        
      >
        <template v-slot:activator>
          <v-list-item-title style="font-size:15px"><v-icon medium color="#0b55d3 "> mdi-clipboard-text-multiple</v-icon> Program</v-list-item-title>
        </template>

          <template >
             <router-link
                to="/program/fullstack-developer"
                class="text-decoration-none"
              >
                <v-list-item  >
                  <v-list-item-title><v-icon medium color="black " class="mr-2">mdi-language-java</v-icon> Fullstack developer</v-list-item-title>
                </v-list-item>
              </router-link>
          </template>
          <template>
            <router-link
                to="/program/python-developer"
                class="text-decoration-none"
              >
                <v-list-item>
                  <v-list-item-title> <v-icon medium color="black " class="mr-2">mdi-language-python</v-icon> Python developer</v-list-item-title>
                </v-list-item>
              </router-link>
          </template>
          <template>
            <router-link
                to="/program/frontend-developer"
                class="text-decoration-none"
              >
                <v-list-item  >
                  <v-list-item-title><v-icon medium color="black " class="mr-2"
            >mdi-language-javascript</v-icon
          > Frontend developer</v-list-item-title>
                </v-list-item>
              </router-link>
          </template>
          <template>
            <router-link
                to="/program/mobile-developer"
                class="text-decoration-none"
              >
                <v-list-item  >
                  <v-list-item-title><v-icon medium color="black " class="mr-2">mdi-react</v-icon> Mobile developer</v-list-item-title>
                </v-list-item>
              </router-link>
          </template>
          <template   >
            
            <router-link
                to="/program/nodejs-programming"
                class="text-decoration-none"
              >
                <v-list-item >
                  
                  <v-list-item-title><v-icon medium color="black " class="mr-2">mdi-nodejs</v-icon> Nodejs programming</v-list-item-title>
                </v-list-item>
              </router-link>
          </template>
      </v-list-group>
        <!-- coba -->
        <v-list nav dense>
          <v-list-item-group>
            <router-link to="/creation" class="text-decoration-none">
              <v-list-item>
                <v-list-item-title class="#0b55d3 --text "
                  > <v-icon medium color="#0b55d3 ">mdi-creation</v-icon> Karya</v-list-item-title
                >
              </v-list-item>
            </router-link>

            <!-- <router-link to="/activity" class="text-decoration-none">
              <v-list-item>
                <v-list-item-title class="#0b55d3 --text "
                  >Kegiatan</v-list-item-title
                >
              </v-list-item>
            </router-link> -->

            <router-link
              to="/register/syarat"
              class="text-decoration-none "
            >
              <v-list-item>
                <v-list-item-title class="#0b55d3 --text"
                  ><v-icon medium color="#0b55d3 ">mdi-form-select </v-icon> Bootcamp</v-list-item-title
                >
              </v-list-item>
            </router-link>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-card>
  </div>
</template>

<script>
import logo from "@/assets/p.png";

export default {
  data: () => {
    return {
      sideNav: false,
      logo,
    };
    
  },
};
</script>

