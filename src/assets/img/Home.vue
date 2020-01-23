<template>
    <div class="page">
        <div class="container">
            <div class="logo">
                <img src="../assets/img/logo.svg" alt="logo" class="logo-image">
            </div>
            <div class="document">
                <img src="../assets/img/delo.svg" alt="document" class="document-image">
            </div>
            <section class="info">
                <div class="info-item line oneLine">
                    <div class="info-item__title">Полное ФИО</div>
                    <div class="info-item__text">Винников Евгений Владимирович</div>
                </div>
                <div class="info-item line toLine">
                    <div class="info-item__title">Год рождения</div>
                    <div class="info-item__text">1993</div>
                </div>
                <div class="info-item line line-3">
                    <div class="info-item__title">Место жительства</div>
                    <div class="info-item__text">г.Москва</div>
                </div>
                <div class="info-item line line-4">
                    <div class="info-item__title">Скайп</div>
                    <div class="info-item__text">critical Error</div>
                </div>
                <div class="info-item line line-5">
                    <div class="info-item__title">Почта</div>
                    <div class="info-item__text">Evinikov@inbox.ru</div>
                </div>
            </section>
            <div class="skill">
              <div class="skill-title">Расскажите о себе чекбоксами</div>
              <p class="skills-text_description">Отметьте только те технологии и типы задач, с которыми вы хорошо знакомы. Отсутсвие опыта отнюдь не означает, что у вас меньше шансов стать нашим сотрудником. Это означает, что вы будете получать те задачи, с которыми гарантировано будете справляться.</p>
              <Checkbox />
            </div>
            <div >
              <p class="slider-title">Уровень владения JavaScript</p>
              <Slider />
                <div class="slider-text">
                  <p class="slider-text_item1">
                    Не владею
                  </p>
                  <p class="slider-text_item2">
                    Использую готовые решения
                  </p>
                  <p class="slider-text_item3">
                    Использую готовые решения и умею их переделывать
                  </p>
                  <p class="slider-text_item4">
                    Пишу сложные JS c нуля
                  </p>
                </div>
            </div>
            <footer class="main-footer">
             <div class="date">
             <div class="date-item1">Дата заполенения</div>
              <div class="date-item2">23.01.2020</div>
            </div>
         </footer>
        </div>
    </div>
</template>


<style lang="scss" >
@import url('https://fonts.googleapis.com/css?family=PT+Sans&display=swap');
@font-face {
  font-family:"Courier New";
  src: url("../assets/7170.ttf");
}


*{
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
}

body{
  background: url("../assets/img/background.svg");
}
.page{
    width: 1000px;
    height: 1314px;
    background: url("../assets/img/anketa.svg") no-repeat 49%;
    margin: 0 auto;
}
.container{
    width: 770px;
    height: 100%;
    margin: 0 auto;
    padding: 50px 0px 0px 0px;
}
.logo{
    width: 77px;
    height: 77px;
    margin-bottom: 40px;
}

.document {
  width: 250px;
  margin: 0 auto;
  margin-bottom: 40px;
}
.info {

  &-item{
    width: 100%;
    display: flex;
    justify-content: flex-start;
    margin-bottom: 29px;
    
    &__title{
      margin-right: 10px;
      font-size: 22px;
      color: #2f1b15;
      font-family: "PT Sans";
      font-weight: 700;
    }
    &__text{
      padding-left: 10px;
      font-size: 30px;
      width: 550px;
      color: #231f20;
      font-family: "Courier New";
    }
  }
}

.line {
  background: url("../assets/img/line.svg") no-repeat;
  background-position-y: 30px;
}

.oneLine{
  background-position-x: 135px;
}
.toLine{
  background-position-x: 142px;
}

.line-3{
  background-position-x: 180px;
}

.line-4{
  background-position-x: 70px;
}
.line-5{
  background-position-x: 70px;
}

.skills-select__block {
    float: left;
    width: 240px;
    margin-right: 25px;
    font-size: 21px;
    color: #000000;
    font-family: "PT Sans";
    font-weight: 700;

      &:nth-child(2) {
        margin-right: 20px;
      }
      &:last-child{
        margin-right: 0px;
      }
}

.skill-title{
  font-size: 24px;
line-height: 50px;
color: #2f1b15;
font-family: "PT Sans";
font-weight: 700;
}

.skills-text_description{
  width: 773px;
  height: 63px;
  font-size: 15px;
  line-height: 23px;
  color: #3d3d3d;
  font-family: "PT Sans";
  font-weight: 400;
  margin-bottom: 35px;
}

.skills-select__block{
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  height: 140px;
  width: 100%;
}

.skill{
  height: 270px;
}

input[type="checkbox"] {
  display: none;
}
 
 label {
 font-size: 21px;
  line-height: 25px;
  font-family: "PT Sans";
  font-weight: 700;
  color: #000;
  cursor: pointer;
  padding: 10px 0;
  vertical-align: middle;
}
input[type="checkbox"] + label:before {
  content: " ";
  display: inline-block;
  margin-right: 15px;
  position: relative;
  text-align: center;
  text-indent: 0px;
  width: 25px;
  height: 25px;
  background: url("../assets/img/check.svg") no-repeat;
  vertical-align: middle;
  background-position-y: 2px
}

input[type="checkbox"]:checked + label:before {
  content:url("../assets/img/mark.svg");
}

/*Slider*/

input[type=range] {
  -webkit-appearance: none;
  width: 100%;
  background: none;
}

input[type=range]::-webkit-slider-thumb {
  
}

input[type=range]::-ms-track {
  width: 100%;
  cursor: pointer;
  background: transparent;
  border-color: transparent;
  color: transparent;
}

input[type=range]::-webkit-slider-thumb {
  -webkit-appearance: none;
  height: 20px;
  width: 20px;
  background: url("../assets/scroll.svg") no-repeat;
  cursor: pointer;
}

.slider-title {
  margin: 0;
  margin-bottom: 31px;
  padding-left: 11px;

  font-weight: 700;
  font-size: 22.43px;
  line-height: 49.83px;
  color: #2f1b15;
}

.slider-text {
  position: relative;
  font-weight: 700;
  font-family: "PT Sans";
  font-size: 13px;
  color: #2f1b15;
  background: url("../assets/slider.svg") no-repeat;
  height: 100px;
}

.slider-text_item1 {
  position: absolute;
  top: 30px;
  left: 0px;

  margin: 0;
}

.slider-text_item2 {
  position: absolute;
  top: 30px;
  left: 148px;
  margin: 0;
}

.slider-text_item3 {
  position: absolute;
  top: 30px;
  left: 385px;

  width: 176px;
  margin: 0;
}

.slider-text_item4 {
  position: absolute;
  top: 30px;
  right: 0px;

  margin: 0;
}

.main-footer {
  padding-top: 10px;
  padding-bottom: 64px;
}

.date {
  font-size: 0;
}

.date-item1 {
  display: inline-block;
  padding-top: 6px;

  font-weight: 700;
  font-size: 22.43px;
  line-height: 49.83px;
  vertical-align: top;
  color: #2f1b15;
}

.date-item2 {
  display: inline-block;
  padding: 5px 15px;
  padding-bottom: 5px;

  font-weight: 400;
  font-size: 30px;
  line-height: 36px;
  font-family: "Courier New", "Courier", monospace;
  vertical-align: top;
  color: #231f20;

  background: url("../assets/line.svg") no-repeat;
  background-position-y: 35px;
  background-position-x: 20px;

}
</style>

<script>

import Checkbox from "../components/Checkbox.vue";
import Slider from "../components/Slider.vue";

export default {
  components: {
    Checkbox,
    Slider
  }
}
</script>