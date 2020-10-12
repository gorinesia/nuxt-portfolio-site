<template>
  <div id="top">
    <v-container fluid>
      <v-card width="100vw">
        <v-img
          class="white--text align-end text-center font-italic"
          :class="{'headline': $vuetify.breakpoint. smAndDown, 'display-1': $vuetify.breakpoint. mdAndUp}"
          src="@/assets/images/Top-background.jpg"
        >
          <p>Practice Makes Perfect</p>
          <p>継続は力なり</p>
        </v-img>
      </v-card>
    </v-container>
  </div>
</template>
