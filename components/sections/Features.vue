<template>
  <section class="purple lighten-2 white--text py-16">
    <v-container>
      <v-row>
        <v-col class="text-center">
          <h2 class="text-h4 text-md-h3 text-center font-weight-black">
            Transformando Vidas: Tu Guía Hacia la Sanación Mental y Física
          </h2>
          <div
            class="text-h5 text-md-h4 text-center font-weight-black py-3 mb-10"
          ></div>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          v-for="(card, index) in cards"
          :key="index"
          cols="12"
          sm="4"
          class="text-center"
        >
          <v-avatar
            size="80"
            class="display-1 white font-weight-bold primary--text mb-5"
            style="opacity: 1.15"
            >{{ card.callout }}</v-avatar
          >
          <div class="title text-uppercase mt-1 mb-4" v-text="card.title"></div>

          <p v-text="card.text"></p>
          <v-row no-gutters>
            <v-col cols="12"> </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row no-gutters>
        <!-- Botón para redirigir a la página de registro -->
        <v-btn
          x-large
          rounded
          color="white"
          class="primary--text mx-auto mt-10 px-16"
        >
          <router-link to="/register">
            <v-icon dark left>mdi-check-bold</v-icon>Registrate
          </router-link>
        </v-btn>

        <!-- Botón para redirigir a la página de inicio de sesión -->
        <v-btn
          x-large
          rounded
          color="white"
          class="primary--text mx-auto mt-10 px-16"
        >
          <router-link to="/login">
            <v-icon dark left>mdi-check-bold</v-icon>Iniciar Sesión
          </router-link>
        </v-btn>
      </v-row>
    </v-container>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: 'Material Design',
          subtitle: 'Best Productivity',
          text: 'Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.',
          callout: '01',
        },
        {
          title: 'Affordable Prices',
          subtitle: 'Special Offers',
          text: 'Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.',
          callout: '02',
        },
        {
          title: 'Fast Loading',
          subtitle: 'Income Flow',
          text: 'Similique sunt in culpa qui officia deserunt mollitia animi, id est laborut dolorum fuga.harum quidem rerum facilis estexpedita distinctio.',
          callout: '03',
        },
      ],
    }
  },
}
</script>
