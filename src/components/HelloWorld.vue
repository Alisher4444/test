<template>
  <div class="app">

    <div class="header">
      <div class="logo">
        <img src="../assets/Logo.svg" alt="">
      </div>
      <div class="links">
        <ul>
          <li>
            <a href="#">Главная</a>
          </li>
          <li>
            <a href="#">Наши преимущества</a>
          </li>
          <li>
            <a href="#">История Exline</a>
          </li>
          <li>
            <a href="#">Нам доверяют</a>
          </li>
          <li>
            <a href="#">Контакты</a>
          </li>
        </ul>
        <ul class="call_to_action">
          <li>
            <a href="#">info@exline.kz</a>
          </li>
          <li>
            <a href="#">+7 (777) 707 87 77</a>
          </li>
        </ul>
      </div>
    </div>
   
    <div class="background">
      
   
    </div>

    <div class="filter">
      <div class="calc">
        <div class="calc-item">
          <p>Рассчитать стоимость</p>
        </div>
        <div class="calc-item">
          <p>Вызвать курьера</p>
        </div>
        <div class="calc-item">
          <p>Отследить посылку</p>
        </div>
      </div>
        <div class="filter-content">
          <div>
          <input type="text" placeholder="Откуда">
          <div class="tags">
            <div class="tag">
              <p>Астана</p>
            </div>
            <div class="tag">
              <p>Алматы</p>
            </div>
            <div class="tag">
              <p>Шымкент</p>
            </div>
          </div>
        </div>
        <button class="switch">
          <img src="../assets/arrow-left-right.svg" alt="">
        </button>
        <div>
          <input type="text" placeholder="Куда">
          <div class="tags">
            <div class="tag">
              <p>Астана</p>
            </div>
            <div class="tag">
              <p>Алматы</p>
            </div>
            <div class="tag">
              <p>Шымкент</p>
            </div>
          </div>
        </div>
        <button class="search">Рассчитать стоимость</button>
        </div>
      </div>

      <div class="advantages">
        <h1>Наши преимущества</h1>
        <div class="advantages-content">
          <div class="item">
            <img src="../assets/fast-delivery-2.svg" alt="">
            <p>Быстрая доставка</p>
          </div>
          <div class="item">
            <img src="../assets/fast-delivery-4.svg" alt="">
            <p>Доставим в любую точку города и области</p>
          </div>
          <div class="item">
            <img src="../assets/fast-delivery-1.svg" alt="">
            <p>Ежедневные отправки</p>
          </div>
          <div class="item">
            <img src="../assets/fast-delivery-3.svg" alt="">
            <p>Собственный склад</p>
          </div>
        </div>
        
      </div>

      <div class="history">
        <h1>История Exline</h1>
        <div class="history-content">
          <div class="item">
            <div class="item-txt">
              <p class="item-txt-title">Курьерская компания Exline основана 31 июля 2003 года</p>
              <p class="item-txt-full">За время работы компания Exline заняла достойную нишу на рынке почтовых услуг, зарекомендовав себя как надежного партнера, которому доверяют свои отправления многие компании казахстанского и международного бизнеса</p>
            </div>
            <img src="../assets/first.jpg" alt="">
          </div>
          <div class="item">
            <img src="../assets/second.jpg" alt="">
            <div class="item-txt">
              <p class="item-txt-title">Курьерская компания Exline основана 31 июля 2003 года</p>
              <p class="item-txt-full">За время работы компания Exline заняла достойную нишу на рынке почтовых услуг, зарекомендовав себя как надежного партнера, которому доверяют свои отправления многие компании казахстанского и международного бизнеса</p>
            </div>
          </div>
        </div>
      </div>

      <div class="partners">
        <h1>Нам доверяют </h1>
        <div class="partners-content">
          <img src="../assets/techno.svg" alt="">
          <img src="../assets/kaspi.svg" alt="">
          <img src="../assets/astanamotors.svg" alt="">
          <img src="../assets/zepter.svg" alt="">

          <img src="../assets/gazprom.svg" alt="">
          <img src="../assets/philips.svg" alt="">
          <img src="../assets/kaztranscom.svg" alt="">
          <img src="../assets/microsoft.svg" alt="">
        </div>
      </div>

      

  </div>
</template>

<script>
export default {
  name: 'App',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


  .header {
    /* width: 100%; */
    height: 80px;
    background-color: white;

    display: flex;
    flex-direction: row;
    /* justify-content: space-between; */
    padding-left: 168px;
    padding-right: 168px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;

    align-items: center;
  }

  .links {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: flex-end;
  }

  ul {
    display: flex;
    flex-direction: row;
    list-style-type: none;
    padding-left: 0;
  }

  li {
    margin-left: 20px;
  }

  a {
    text-decoration: none;
    color: #000;
  }

  .call_to_action {
    border-left: 1px solid #ccc;
    /* padding-left: 10px; */
    margin-left: 20px;
  }

  .call_to_action a {
    color: #583899;
  }

  .background {
    width: 100%;
    height: 600px;
    background-color: #ccc;
  }

  .filter {
    width: fit-content;
    filter: drop-shadow(0px 4px 15px rgba(0, 0, 0, 0.1));

    margin: 0 auto;

    position: relative;
    top: -100px;
  }

  .filter-content {
    display: flex;
    flex-direction: row;
    padding: 20px 30px;
    background: #FFFFFF;
    border-radius: 0px 12px 12px 12px;

  }

  .calc {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
  }

  .calc-item {
    width: 195px;
    height: 48px;
    

    font-family: 'Mulish';
    font-style: normal;
    font-weight: 700;
    font-size: 14px;
    line-height: 18px;
    /* identical to box height, or 129% */

    text-align: center;
    background: #F6F6F6;
    
  }

  .calc-item:hover {
    background: #FFFFFF;
    color: #EF363C;
  }

  .calc-item:first-child {
    border-radius: 12px 0 0 0 ;
  }

  .calc-item:last-child {
    border-radius: 0 12px 0 0;
  }

  

  .tags {
    display: flex;
    flex-direction: row;
    margin-top: 12px;
  }
  .tag {
    /* height: 30px; */
    padding: 6px 12px;
    background: #F6F6F6;
    border-radius: 12px;
    margin-right: 12px;

    font-family: 'Mulish';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 18px;
    /* identical to box height, or 129% */


    color: #000000;
  }

  .tag p {
    margin: 0;
  }
  .switch {
    width: 50px;
    height: 50px;
    background-color: transparent;
    border: 0;
  }

  .search {
    width: 276px;
    height: 48px;
    left: 768px;
    top: 0px;

    background: #EF363C;
    border-radius: 12px;

    font-family: 'Mulish';
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
    /* identical to box height, or 125% */

    text-align: center;
    outline: none;
    border: 0;
    color: #FFFFFF;

    margin-left: 24px;
  }

  input {
    width: 350px;
    height: 48px;
    left: 394px;
    top: 0px;

    background: #FFFFFF;
    border: 1px solid #CBCBCB;
    border-radius: 12px;

    font-family: 'Mulish';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 18px;
    /* identical to box height, or 129% */
    padding-left: 20px;
    outline: 0;
    color: #000000;
  }

  input::placeholder {
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 18px;
    /* identical to box height, or 129% */


    color: #000000;
  }

  .advantages {
    padding-left: 168px;
    padding-right: 168px;
    margin-top: 60px;
  }


  .advantages-content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-top: 30px;
  }
  .advantages h1 {
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 28px;
    /* identical to box height, or 117% */
    text-align: start;

    color: #000000;
  }

  .advantages .item{
    padding: 20px 16px;
    background: #F6F6F6;
    border-radius: 12px;
    margin-right: 24px;
  }

  .advantages .item:last-child{ margin-right: 0;}

  .advantages .item p{
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 20px;
    /* or 125% */
    width: 226px;
    text-align: center;

    color: #000000;
  }

  .history {
    padding-left: 168px;
    padding-right: 168px;
    margin-top: 60px;
  }

  .history-content {
    /* width: 100%; */
    display: grid;
    grid-template-columns: 1fr 2fr;
  }
  .history h1 {
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 28px;
    /* identical to box height, or 117% */

    text-align: start;
    color: #000000;

  }

  .history-content .item {
    /* width: 446px; */
    margin-right: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .history-content .item:last-child {
    /* width: 446px; */
    margin-right: 0px;
  }

  .history-content .item img {
    border-radius: 12px;
  }

  .history-content .item-txt {
    
    /* height: 222px; */
    background: #F6F6F6;
    border-radius: 12px;
    padding: 30px;
    margin-bottom: 24px;
  }

  .history-content .item-txt:last-child {
    margin-bottom: 0;
    margin-top: 24px;
  }

  .item-txt-title {
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 28px;
    /* or 117% */


    color: #000000;
  }

  .item-txt-full{
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 18px;
    /* or 129% */

    text-align: justify;
    color: rgba(0, 0, 0, 0.75);

  }

  .partners {
    padding-left: 168px;
    padding-right: 168px;
    margin-top: 60px;
  }

  .partners h1 {
    text-align: start;
    font-family: 'Mulish';
    font-style: normal;
    font-weight: 800;
    font-size: 24px;
    line-height: 28px;
    /* identical to box height, or 117% */


    color: #000000;
  }

  .partners-content {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
  
</style>
