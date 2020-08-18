<template>
  <div class="about">
    <div class="title-container">
      <h1>Hi, I am Angela Fei</h1>
      <p>Front-end developer with over 6 years of commercial experience working in UK, Australia and Taiwan.</p>
      <p>Love nature and simplicity.</p>
      <router-link to="/skills">
        <button>My skill set</button>
      </router-link>
      <!-- <div class="arrow-container">
        <div class="arrow"></div>
      </div> -->
    </div>
  </div>
</template>

<style lang="scss">
  .about {
    padding: 2rem;
    min-height: 100vh;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    background: url('../assets/images/bg3.png') 80% 76% no-repeat;

    .title-container {
      display: flex;
      align-items: center;
      text-align: center;
      flex-direction: column;

      h1 {
        font-family: 'ftnk';
        font-size: 70px;
        font-style: normal;
        font-weight: bold;
        line-height: 70px;
      }

      p {
        padding: 2rem;
        line-height: 2rem;
        font-size: 1.2rem;
      }

      button {
        border: none;
        border-radius: 2rem;
        padding: 1rem 1.2rem;
        background-color: #6bd3ea;
        color: white;
        cursor: pointer;
        font-size: 1rem;
      }
    }

    // .arrow-container {
    //   cursor: pointer;
    //   width: 100%;
    //   height: 40px;
    //   display: flex;
    //   justify-content: center;
    // }

    // .arrow {
    //   transform: rotate(45deg) translateY(-15px) translateX(5px);
    //   // bottom: 5px;
    //   height: 30px;
    //   // position: absolute;
    //   width: 30px;
    //   border-bottom: 1px solid #333;
    //   border-right: 1px solid #333;
    // }
  }
</style>
