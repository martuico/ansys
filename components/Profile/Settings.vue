<template>
  <div class="settings">
    <img src="/img/pen.png" class="icon" alt="pen">
    <h2>{{ title }}</h2>
    <ul>
      <li v-for="(li, liInd) in list" :key="liInd">{{ li }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title must be here'
    },
    list: {
      type: Array,
      default: []
    }
  }
}
</script>

<style lang="scss" scoped>
  .settings {
    border: 1px solid #000000;
    padding: 25px;
    position: relative;
    margin-top: 3em;
    margin-bottom: 3em;

    h2 {
      font-family: 'Krona One';
      font-style: normal;
      font-weight: normal;
      font-size: 20px;
      line-height: 25px;
      display: flex;
      align-items: center;
      text-transform: lowercase;

      color: #000000;
    }

    .icon {
      width: 32px;
      height: 32px;
      position: absolute;
      top: 20px;
      right: 20px;
    }

    ul {
      list-style: none;
      columns: 3;
      -webkit-columns: 3;
      -moz-columns: 3;
      li {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 25px;
      }
    }
  }
</style>
