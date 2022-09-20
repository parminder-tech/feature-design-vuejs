<template>
  <div class="card">
    <div class="img">
      <img :src="cardItem.img" alt="" />
    </div>
    <div class="details">
      <div class="title">{{cardItem.title}}</div>
      <ul>
        <li v-for="(item, index) in cardItem.list" :key="index">{{item}}</li>
      </ul>
      <p>{{cardItem.desc}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:{
        cardItem:{}
    }
};
</script>

<style lang="scss">
.card {
  display: flex !important;
  overflow: hidden;
  background: #ffffff;
  border-radius: 8px;
  img {
    height: 100%;
  }
  .details {
    padding: 1.5rem;
    .title {
      font-weight: 700;
      font-size: 24px !important;
      color: #353844;
    }
    ul {
      list-style-type: none;
      margin-bottom: 0;
      margin-bottom: 0.5rem;
      padding: 0;
    }
    li {
      font-family: "Nunito Sans", sans-serif !important;
      font-weight: 700;
      font-size: 15px;
      line-height: 26px;
      color: #353844;
      position: relative;
      padding-left: 1rem;
      &::before{
        position: absolute;
        content: '';
        height: 6px;
        width: 6px;
        background: #D2AD81;
        left: 0;
        top: 50%;
        border-radius: 50%;
        transform: translateY(-50%);
      }
    }
    p {
      font-family: "Nunito Sans", sans-serif !important;
      font-style: normal;
      font-weight: 600;
      font-size: 15px;
      line-height: 24px;
      color: #353844;
    }
  }
}
</style>