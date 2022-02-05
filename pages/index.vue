<template>
<div>
  <v-row justify="center" align="center">
    <h1>Всех приветствуем на сайте<br> фермерского роддома номер 5</h1>
    <p v-html="text"></p>
    <v-img :src="img"></v-img>
  </v-row>
  <v-row justify="left" align="left">  
     <div class="footer">
            <p>Контакты</p>
            <p>
                Телефон: 8(000)000-00-00<br>
                Почта: ferm@rodi.ru<br>
                Инстаграм: ferm_rodi_123
            </p>
      </div> 
  </v-row>
</div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters({ text: 'info/getInfoText', img: 'info/getInfoImg' }),
  },
  async mounted() {
    this.$store.dispatch('info/getInfo', 'home_page')
  },
}
</script>
<style scoped>
 h1{
    text-align: center;
    padding: 100px 20px;
    color: #000;
    font-family: "Roboto";
  }
</style>
