<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col-6">
            <q-img
            transition="jump-up"
            src="~assets/images/skill/skill.webp"
            style="width: 100%;height:45vh"
            >
            <!-- <div class="absolute-bottom text-subtitle1 text-center text-bold">
                skill
            </div> -->
            </q-img>
          </div>
          <div class="col-6">
              <div class="q-ma-md text-grey-4">
                  <h1><u>{{ title }}</u></h1>
              </div>
              <div class="q-ma-md text-grey-10 text-bold">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row q-pa-lg' >
        <div class="col-2 q-pa-md col-md-2 col-xs-6" :key="skil" v-for="skil in skill">
          <q-card class="my-card text-center">
            <q-circular-progress
              show-value
              font-size="40px"
              class="q-ma-md"
              :value="skil.value"
              size="60px"
              :thickness="0.20"
              color="primary"
              track-color="grey-3"
            >
              <q-avatar size="100%">
                <img :src="skil.img">
              </q-avatar>
            </q-circular-progress>

            <q-card-actions class="justify-center">
              <q-btn flat class="">{{ skil.name }}</q-btn>
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
      title: 'Mes compétances:',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.',
      skill: [
        {
          name: 'LINUX',
          img: 'images/skill/linux.png',
          value: 80
        },
        {
          name: 'HTML',
          img: 'images/skill/html.png',
          value: 80
        },
        {
          name: 'CSS',
          img: 'images/skill/css.png',
          value: 80
        },
        {
          name: 'GRID/FLEX',
          img: 'images/skill/flex_grid.png',
          value: 60
        },
        {
          name: 'SASS',
          img: 'images/skill/sass.jpeg',
          value: 70
        },
        {
          name: 'NGINX',
          img: 'images/skill/nginx.png',
          value: 60
        },
        {
          name: 'LINUX-SERVER',
          img: 'images/skill/linux_server.jpeg',
          value: 20
        },
        {
          name: 'BOOTSTRAP',
          img: 'images/skill/bootstrapp.png',
          value: 80
        },
        {
          name: 'NodeJs',
          img: 'images/skill/nodejs.png',
          value: 50
        },
        {
          name: 'Java Script',
          img: 'images/skill/js.png',
          value: 5
        },
        {
          name: 'Quasar',
          img: 'images/skill/quasar.png',
          value: 10
        },
        {
          name: 'VueJs',
          img: 'images/skill/vuejs.png',
          value: 5
        },
        {
          name: 'MongoDB',
          img: 'images/skill/mongodb.png',
          value: 1
        }
      ]
    }
  }
}
</script>
