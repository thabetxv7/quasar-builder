<template>
  <q-page class="flex flex-center q-mx-lg">
    <div class="q-my-md">
      <img
        alt="Quasar logo"
        src="~assets/quasar-logo-vertical.svg"
        style="width: 200px; height: 200px"
      >
    </div>
    <div>
      <p>Count: {{ count }}</p>
    </div>
    <q-btn color="primary" @click="count = count +5">Plus 5 Chart</q-btn>
    <q-btn to="./sss">Go to 404</q-btn>
    <div class="row ">
      <bar-chart v-for="(x,i) in count" :key="-i" class="col-6"/>
    </div>
  </q-page>
</template>

<script>
import {defineComponent} from 'vue'
import BarChart from "components/chartBar";

export default defineComponent({
  name: 'IndexPage',
  components: {BarChart},
  data() {
    return {
      count: 5,
    }
  }
})
</script>
