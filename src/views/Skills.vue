<template>
  <div class="skills-container">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <h2>Skills</h2>
    <p class="guide">Click to Flip card and see details</p>
    <div class="skill-group">
      <h3>Programming (Front-end)</h3>
      <ul>
        <li>
          <SkillItem :percentage="85" type="reactjs">
            <p>Experience: 2.5 years</p>
            <p>Project: <a href="https://www.nowtv.com/" target="_blank">NowTV website</a></p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="angularjs">
            <p>experience: 2 years</p>
            <p>Project: <a href="https://www.dudooeat.com/" target="_blank">Dudoo webapp and POS</a></p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="55" type="vuejs">
            <p>experience: 2 weeks</p>
            <p>Project: <a href="#" target="_blank">This website you are currently browsing</a></p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="90" type="html5">
            <p>experience: 10 years</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="65" type="graphql">
            <p>experience: 3 months</p>
            <p>Project: <a href="https://stackla.com/" target="_blank">Stackla's AI-powered enterprise UGC platform</a></p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="75" type="map libraries">
            <p>experience: 1.5 years</p>
            <p>Projects:
              <a href="https://www.dudooeat.com/" target="_blank">Dudoo webapp</a>
              <a href="https://cameo.tw/3/ai/case-02.html" target="_blank">Data Analysis (Cameo)</a>
            </p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="charts libraries">
            <p>experience: 6 months</p>
            <p>Project:
              <a href="https://cameo.tw/3/ai/case-02.html" target="_blank">Data Analysis (Cameo)</a>
            </p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="65" type="other libraries">
            <p>experience: 6 months</p>
            <p>Projects:
              <a href="https://www.dudooeat.com/" target="_blank">Dudoo POS</a>,
              <span>Internal Project in Hon-Hai (Foxconn)</span>
            </p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Programming (Back-end-end)</h3>
      <ul>
        <li><SkillItem :percentage="70" type="nodejs" /></li>
        <li><SkillItem :percentage="50" type="php" /></li>
        <li><SkillItem :percentage="50" type="python" /></li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Styling</h3>
      <ul>
        <li><SkillItem :percentage="85" type="css3" /></li>
        <li><SkillItem :percentage="70" type="bootstrap" /></li>
        <li><SkillItem :percentage="70" type="tailwind" /></li>
        <li><SkillItem :percentage="90" type="sass" /></li>
      </ul>
    </div>
    <!-- <div class="skill-group">
      <h3>Testing</h3>
      <ul>
        <li><SkillItem :percentage="90" type="mocha" /></li>
        <li><SkillItem :percentage="90" type="chai" /></li>
        <li><SkillItem :percentage="75" type="cypress" /></li>
        <li><SkillItem :percentage="85" type="selenium" /></li>
        <li><SkillItem :percentage="50" type="robot framework" /></li>
      </ul>
    </div> -->
    <div class="skill-group">
      <h3>Other Tools</h3>
      <ul>
        <li><SkillItem :percentage="80" type="gulp" /></li>
        <li><SkillItem :percentage="85" type="git" /></li>
        <li><SkillItem :percentage="75" type="webpack" /></li>
        <li><SkillItem :percentage="70" type="babel" /></li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Adobe Creative Suites</h3>
      <ul>
        <li><SkillItem :percentage="75" type="photoshop" /></li>
        <li><SkillItem :percentage="70" type="illustrator" /></li>
        <li><SkillItem :percentage="80" type="dreamweaver" /></li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>OS</h3>
      <ul>
        <li><SkillItem :percentage="85" type="mac" /></li>
        <li><SkillItem :percentage="70" type="windows" /></li>
        <li><SkillItem :percentage="75" type="linux" /></li>
      </ul>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import SkillItem from '@/components/SkillItem.vue'

export default {
  name: 'Skills',
  components: {
    SkillItem
  }
}
</script>

<style scoped lang="scss">
.skills-container {
  padding: 2rem;

  h2 {
    font-size: 2rem;
    font-weight: bold;
  }

  .guide {
    padding: 1rem 0;
  }

  .skill-group {
    padding: .5rem 1rem;

    h3 {
      padding: .8rem 0;
    }

    li + li {
      padding-top: .3rem;
    }
  }
}
</style>
