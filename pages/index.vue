<template>
  <div>
        <main>
          <aside>
              <h2>В нашем роддоме ежедневно рождаются десятки милейших зверушек</h2>
              <p class="aside_text">Теленок</p>
              <img src="@/assets/images/left_widget_img.jpg" alt="animal" class="animal">
          </aside> 
          <div class="header">
          <h1>Всех приветствуем на сайте<br> фермерского роддома номер 5</h1>
           <img src="@/assets/images/home_page_img.jpg" alt="animal" class="animalHead">
          </div> 
          <p class="text">Значимость этих проблем настолько очевидна, что дальнейшее развитие различных форм
            деятельности обеспечивает широкому кругу (специалистов) участие в формировании новых
              предложений. Повседневная практика показывает, что реализация намеченных плановых
              заданий в значительной степени обуславливает создание модели развития.<br><br>
              Значимость этих проблем настолько очевидна, что дальнейшее развитие различных форм
              деятельности обеспечивает широкому кругу (специалистов) участие в формировании новых
                предложений. Идейные соображения высшего порядка, а также дальнейшее развитие различных
                форм деятельности позволяет оценить значение новых предложений.<br><br>
              С другой стороны постоянное информационно-пропагандистское обеспечение нашей
              деятельности обеспечивает широкому кругу (специалистов) участие в формировании
                позиций, занимаемых участниками в отношении поставленных задач. С другой
                стороны рамки и место обучения кадров способствует подготовки и реализации модели развития.
          </p>
        </main>
        <div class="footer">
            <p>Контакты</p>
            <p>
                Телефон: 8(000)000-00-00<br>
                Почта: ferm@rodi.ru<br>
                Инстаграм: ferm_rodi_123
            </p>
        </div> 
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  head: {
    title: "Главная"
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
  h2{
    text-align: center;
    padding: 20px 0;
    color: #000;
    font-family: "Roboto";
    font-size: 16px;
  }
  .text{
    text-align: left;
    padding: 100px 20px;
    color: #000;
    font-family: "Roboto";
  }
  aside{
    width: 250px;
    border: 3px solid palevioletred;
    background-size: 250px 100%;
    float: right;
    min-height: 110vh;
  }
  .animal{
    width: 200px;
    height: auto;
    margin-left: 30px;
  }
  .aside_text{
    text-align: center;
    padding-bottom: 10px;
  }
  .footer{
    padding: 0 0 20px 20px;
    height: 70px;
  }
  .animalHead{
      height: 400px;
      margin-left: 180px;
   }
</style>

