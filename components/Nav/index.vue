<template>
  <div class="navbar">
    <div class="logo">
      <LogoWhite />
    </div>

    <div class="search-box">
      <input type="text" class="form-contol" placeholder="search job titles">
    </div>

    <div class="navblock text-right">
      <ul class="nav">
        <li>
          <a>
            <img class="icon" src="/img/1f680.png" alt="">
            explore
          </a>
        </li>
        <li>
          <img class="icon" src="/img/2b50.png" alt="">
          <a>faves</a>
        </li>
        <li>
          <img class="icon" src="/img/1f525.png" alt="">
          <a>trending</a>
        </li>
        <li>
          <img class="icon" src="/img/1f60e.png" alt="">
          <a>u</a>
        </li>
        <li>
          <button class="btn-link">
            0
            <img class="icon" src="/img/1f333.png" alt="">
          </button>
        </li>
      </ul>
    </div>
  </div>
</template>


<style lang="scss">
  .btn-link {
    background: none;
    color: #ffffff;
    padding: 5px 13px;
    border: 1px solid #FFFFFF;
    box-sizing: border-box;
    border-radius: 100px;
  }
  .icon {
    width: 15px;
  }

  .text-right {
    text-align:right;
  }

  .nav {
    list-style-type: none;
    margin: 0;
    padding: 0;
    li {
      display: inline;
      padding: 5px 20px;
      a {
        color: #ffffff;
      }
    }
  }

  .navbar {
    max-height: 75px;
    background: #12198F;
    display: flex;
    padding: 5px 25px;
    align-items: center;

    .logo {
      margin: 0 15px;
    }

    .search-box {
      input {
        background: #FFFFFF;
        border: 1px solid #000000;
        box-sizing: border-box;
        border-radius: 50px;
        height: 35px;
        width: 331px;
        padding: 0 22px;
      }
    }
  }

  .navblock {
    flex-grow: 1;
  }
</style>
