<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col-6 col-xs-12">
            <q-img
            transition="scale"
            src="~assets/images/reseau/reseau.jpeg"
            style="width: 100%;height:45vh"
            >
            <div class="absolute-bottom text-subtitle1 text-center text-bold">
                Rejoignez-moi
            </div>
            </q-img>
          </div>
          <div class="col-6 col-xs-12">
              <div class="q-ma-md text-grey-4">
                  <h4><u>{{ title }}</u></h4>
              </div>
              <div class="q-ma-md text-grey-10 text-bold">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row q-pa-lg' >
        <div class="col-3 q-pa-md col-md-3 col-lg-2 col-sm-4 col-xs-6"
          :key="soc" v-for="soc in social"
        >
          <q-card  class="my-card">
            <q-img :src="soc.img" height="20vh">
              <div class="absolute-bottom">
                <div class="text-h8">{{ soc.name }}</div>
              </div>
            </q-img>

            <q-card-actions>
              <q-btn type="a" :href='soc.link' target="_blank" flat><q-icon class="q-ma-xs" name="visibility"/>View</q-btn>
              <!-- <q-btn flat><q-icon class="q-ma-xs" name="person_add_alt_1"/>Follow</q-btn> -->
            </q-card-actions>
          </q-card>
        </div>
      </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Mes réseaux:',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.',
      social: [
        {
          name: 'Linkedin',
          link: 'https://www.linkedin.com/in/wilfried-zanni-4531b0186',
          img: require('assets/images/reseau/linkedin.webp')
        },
        {
          name: 'Slack',
          link: 'https://slack.com/intl/fr-fr/',
          img: require('assets/images/reseau/slack.png')
        },
        {
          name: 'GitHub',
          link: 'https://github.com/wilfried-72',
          img: require('assets/images/reseau/github.png')
        }
      ]
    }
  }
}
</script>
