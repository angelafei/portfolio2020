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
        <li>
          <SkillItem :percentage="60" type="nodejs">
            <p>experience: 6 months</p>
            <p>Projects:
              <a href="https://help.nowtv.com/article/watching-now-tv-on-a-mac" target="_blank">NowTV Player (using electron)</a>,
              <span>Internal Project in Hon-Hai (Foxconn)</span>
            </p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="60" type="php">
            <p>experience: 6 months</p>
            <p>Project:
              <a href="https://www.dudooeat.com/" target="_blank">Dudoo analysis platform</a>,
            </p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="60" type="python">
            <p>experience: 6 months</p>
            <p>Project:
              <a href="https://www.dudooeat.com/" target="_blank">Dudoo crawler and integration testing</a>
            </p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Styling</h3>
      <ul>
        <li>
          <SkillItem :percentage="85" type="css3">
            <p>experience: 10 years</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="80" type="bootstrap">
            <p>experience: 2 years</p>
            <p>Projects:
              <a href="https://cameo.tw/3/ai/case-02.html" target="_blank">Data Analysis (Cameo)</a>,
              <span>Internal Project in Hon-Hai (Foxconn)</span>
            </p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="tailwind">
            <p>experience: 3 months</p>
            <p>Project: <a href="https://stackla.com/" target="_blank">Stackla's AI-powered enterprise UGC platform</a></p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="90" type="sass">
            <p>experience: 3 years</p>
            <p>Projects:
              <a href="https://www.dudooeat.com/" target="_blank">Dudoo platforms (webapp, analysis platform, POS)</a>,
              <span>Internal Project in Hon-Hai (Foxconn)</span>
            </p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Testing</h3>
      <ul>
        <li>
          <SkillItem :percentage="90" type="mocha">
            <p>experience: 4 years</p>
            <p>unit-testing</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="90" type="chai">
            <p>experience: 4 years</p>
            <p>unit-testing</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="90" type="sinon">
            <p>experience: 4 years</p>
            <p>unit-testing</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="75" type="cypress">
            <p>experience:  6 months</p>
            <p>unit-testing</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="85" type="selenium">
            <p>experience: 1.5 years</p>
            <p>integration-testing, e2e testing, crawler</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="50" type="robot framework">
            <p>experience: 2 months</p>
            <p>integration-testing, e2e testing</p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Other Tools</h3>
      <ul>
        <li>
          <SkillItem :percentage="80" type="gulp">
            <p>experience: 1.5 years</p>
            <p>bundling, code uglify</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="85" type="git">
            <p>experience: 4.5 years</p>
            <p>collabration, version control</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="75" type="webpack">
            <p>experience: 2 years</p>
            <p>bundling, code uglify, optimising</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="babel">
            <p>experience: 2 years</p>
            <p>JavaScript compiler</p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>Adobe Creative Suites</h3>
      <ul>
        <li>
          <SkillItem :percentage="75" type="photoshop">
            <p>experience: 4 years</p>
            <p>image editing</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="illustrator">
            <p>experience: 4 years</p>
            <p>creating drawings, illustrations, and artwork</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="80" type="dreamweaver">
            <p>experience: 3 years</p>
            <p>creating, publishing, and managing websites and mobile content</p>
          </SkillItem>
        </li>
      </ul>
    </div>
    <div class="skill-group">
      <h3>OS</h3>
      <ul>
        <li>
          <SkillItem :percentage="85" type="mac">
            <p>experience: 8 years</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="70" type="windows">
            <p>experience: 10 years</p>
          </SkillItem>
        </li>
        <li>
          <SkillItem :percentage="75" type="linux">
            <p>experience: 2.5 years</p>
          </SkillItem>
        </li>
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
    display: inline-block;
    font-size: 2rem;
    font-weight: bold;
    text-decoration: underline;
    text-underline-position: under;
    padding-bottom: .8rem;
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
