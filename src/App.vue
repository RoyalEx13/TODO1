<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://scontent.fcnx4-1.fna.fbcdn.net/v/t1.15752-9/s206x206/271715900_635230231119596_2084932409548402643_n.jpg?_nc_cat=107&ccb=1-5&_nc_sid=aee45a&_nc_eui2=AeGhNX7yzBLCMJo7KTE1N7jGtzBcg6c25pC3MFyDpzbmkHTa6onOkztY7KVuZcE0_yezyiqe0tdbj86rhj3tz6O5&_nc_ohc=QF-q7x_3vxwAX-k7Ecl&_nc_ht=scontent.fcnx4-1.fna&oh=03_AVK00zHjnDuQspE9kXPqQN8aZGxpuf8wU84agQVWSETWow&oe=621BE491"
          transition="scale-transition"
          width="40"
        />

        <span class="mr-2">ไอ่เล็กการบ้าน</span>
      </div>

      <v-spacer></v-spacer>

      <!-- <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn> -->
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
