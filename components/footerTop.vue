<template>
  <section
    id="footer-top"
    :class="
      $vuetify.theme.dark
        ? 'blue-grey darken-4 grey--text text--lighten-1'
        : 'grey lighten-3 grey--text text--darken-4'
    "
  >
    <v-container>
      <v-row>
        <v-col cols="12" md="5" class="py-12"
          ><v-row no-gutters>
            <v-col cols="12">
              <Logo />
            </v-col>
            <v-col cols="12">
              <p class="mt-8 text-justify" style="max-width: 400px">
                "Descubre un espacio dedicado al bienestar mental y emocional,
                diseñado para proporcionar apoyo, recursos y orientación a
                aquellos que buscan mejorar su calidad de vida. Nuestro sitio
                ofrece una variedad de herramientas, consejos, y acceso a
                expertos en salud mental, todo con el objetivo de ayudarte a
                cultivar una mente más fuerte y resiliente."
              </p>
            </v-col>
            <v-col cols="12">
              <v-list two-line class="transparent">
                <v-list-item>
                  <v-list-item-icon>
                    <v-icon> mdi-map-marker </v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>DIRECCION</v-list-item-title>
                    <v-list-item-subtitle
                      >1400 Main Street, Orlando, FL 79938</v-list-item-subtitle
                    >
                  </v-list-item-content>
                </v-list-item>
                <v-divider></v-divider>
                <v-list-item>
                  <v-list-item-icon>
                    <v-icon> mdi-email </v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>CORREO</v-list-item-title>
                    <v-list-item-subtitle
                      >info@example.com</v-list-item-subtitle
                    >
                    <v-list-item-subtitle
                      >support@example.com</v-list-item-subtitle
                    >
                  </v-list-item-content>
                </v-list-item>

                <v-divider></v-divider>

                <v-list-item>
                  <v-list-item-icon>
                    <v-icon> mdi-phone </v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>TELÉFONO</v-list-item-title>
                    <v-list-item-subtitle>(323) 555-6789</v-list-item-subtitle>
                    <v-list-item-subtitle>(650) 555-1234</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
                <v-divider></v-divider>
              </v-list>
              <div class="d-flex justify-center mt-5">
                <v-btn
                  v-for="(socialm, i) in social"
                  :key="`social-${i}`"
                  class="d-flex"
                  icon
                  large
                  color="primary"
                  :href="socialm.link"
                  target="_blank"
                >
                  <v-icon>{{ socialm.icon }}</v-icon>
                </v-btn>
              </div>
            </v-col>
          </v-row></v-col
        >
        <v-col cols="1" class="text-center hidden-sm-and-down col col-2 py-12">
          <v-divider vertical></v-divider>
        </v-col>
        <v-col cols="12" md="5" class="py-12">
          <h3 class="mb-8">ENVÍA TU MENSAJE</h3>
          <footerContactForm />
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>

<script>
import footerContactForm from '~/components/sections/footerContactForm.vue'
export default {
  components: {
    footerContactForm,
  },
  data() {
    return {
      social: [
        {
          platform: 'Facebook',
          link: 'https://www.facebook.com/',
          icon: 'mdi-facebook',
        },
        {
          platform: 'Twitter',
          link: 'https://twitter.com/',
          icon: 'mdi-twitter',
        },
        {
          platform: 'Instagram',
          link: 'https://www.instagram.com/',
          icon: 'mdi-instagram',
        },
        {
          platform: 'Linkedin',
          link: 'https://www.linkedin.com/',
          icon: 'mdi-linkedin',
        },
        {
          platform: 'Github',
          link: 'https://www.github.com/',
          icon: 'mdi-github',
        },
      ],
    }
  },
}
</script>
