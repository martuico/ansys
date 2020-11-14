<template>
  <div class="container">
    <div class="header">
      <div class="profile-image">
        <img src="/img/profilepic.png" alt="profile">
      </div>
      <h2>george liu</h2>
    </div>
    <div class="content">
      <ul class="navigation">
        <li><a href="#">profile</a></li>
        <li><a href="#">progress</a></li>
        <li class="active"><a href="#">settings</a></li>
      </ul>
      <div class="section-content">
        <Settings v-for="(section,secInd) in sections"
        :key="secInd"
        :title="section.title" :list="section.list" />

        <div class="combine">
          <div>
            <Settings
              :title="'education'"
              :list="['economics','associate degree, 2018','columbia university']"
            />
          </div>
          <div>
            <Settings
              :title="'email'"
              :list="['xl2399@columbia.edu']"
            />
          </div>
        </div>

        <button class="special-btn">change password</button>
      </div>


    </div>
  </div>
</template>

<script>
import Settings from '~/components/Profile/Settings'
export default {
  components: {
    Settings
  },
  computed: {
    problemsList() {
      return ['climate','change','healthcare','poverty','urban mobility','space exploration','cybersecurity','future of food','education','civil liberties','deadly diseases']
    },
    sections() {
      return [
        {title: 'Problems', list: ['climate','change','healthcare','poverty','urban mobility','space exploration','cybersecurity','future of food','education','civil liberties','deadly diseases']},
        {title: 'job locations', list: ['flexible in the u.s.','los angeles, ca','washington dc','new york city, ny ','boston, ma','austin, tx','sf bay area, ca','seattle, wa','remote']},
        {title: 'job types', list: ['full-time','part-time','intership']},
        {title: 'experience', list: ['young + idealistic (0-2 yrs)']},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@font-face {
  font-family: 'Krona One';
  font-style: normal;
  font-weight: 700;
  font-display: swap;
  src: url('~assets/fonts/KronaOne-Regular.ttf') format('truetype');
}

.special-btn {
  margin: 0 auto;
  background: #CCFFF9;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 0px;
  font-family: Work Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 21px;
  display: flex;
  align-items: center;
  text-align: center;
  color: #000000;
  padding: 17px 30px;
  box-shadow: -6px 7px 0px 2px rgba(255,207,204,1);
  -webkit-box-shadow: -6px 7px 0px 2px rgba(255,207,204,1);
  -moz-box-shadow: -6px 7px 0px 2px rgba(255,207,204,1);
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  justify-content: center;
  width: 90%;

  .header {
    margin: 50px auto;

    h2 {
      font-family: 'Krona One';
      font-style: normal;
      font-weight: normal;
      font-size: 50px;
      line-height: 62px;
      align-items: center;
      text-align: center;
      text-transform: lowercase;
    }
  }

  .profile-image {
    background: linear-gradient(90deg, #F1EDFF 0%, #D5FFDE 100%);
    border: 1px solid #000000;
    box-sizing: border-box;
    width: 100px;
    height: 100px;
    border-radius: 50px;
    position: relative;
    margin: 0 auto;

    img {
      width: 58.82px;
      position: absolute;
      top: 27px;
      left: 22px;
    }
  }

  .combine {
    padding: 0;
    margin: 0;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    div {
      flex: 1;
    }
  }

  .content {
    box-sizing: border-box;

    .navigation {
      padding: 0;
      margin: 0;
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      list-style: none;
      text-align: center;
      border-top: 1px solid #000000;
      border-left: 1px solid #000000;
      border-bottom: 1px solid #000000;


      li {
        flex: 1;
        border-right: 1px solid #000000;
        padding: 20px 47px;
        font-family: 'Krona One';
        font-style: normal;
        font-weight: normal;
        font-size: 30px;
        line-height: 37px;
        a {
          text-decoration: none;
          color: #000000;
          display: block;
        }

        &.active {
          background: #E7FFE8;
          box-sizing: border-box;
        }

        &:hover{
          background: #E7FFE8;
          box-sizing: border-box;
        }
      }
    }

    .section-content {
      border-right: 1px solid #000000;
      border-bottom: 1px solid #000000;
      border-left: 1px solid #000000;
      min-height: 10vh;
      padding: 20px 80px;
    }
  }
}

</style>
