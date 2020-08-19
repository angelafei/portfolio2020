<template>
  <div>
    <div class="scene">
      <div v-bind:class="{ card: true, 'is-flipped': isActive }" v-on:click="isActive = !isActive">
        <div class="card__face card__face--front">
          <div class="skill-item-container">
            <div class="skill-type-container">
              <img :src="require(`@/assets/images/${type}.png`)" />
              <span class="type-name">{{type}}</span>
            </div>
            <div class="percentage-container">
              <span class="percentage" :style="{ width: percentage + '%', background: '#6bd3ea' }"></span>
              <span class="hidden-percentage" :style="{ width:  (100 - percentage) + '%', background: 'white' }"></span>
            </div>
          </div>
        </div>
        <div class="card__face card__face--back">
          <div class="text-container">
            <slot></slot>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SkillItem',
  props: {
    percentage: Number,
    type: String
  },
  data () {
    return {
      isActive: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.scene {
  height: 100px;
  perspective: 600px;
  // border-radius: .2rem;
  // overflow: hidden;
  padding: 5px;
}

.card {
  position: relative;
  width: 100%;
  height: 100%;
  cursor: pointer;
  transform-style: preserve-3d;
  transform-origin: center right;
  transition: transform 1s;
}

.card.is-flipped {
  transform: translateX(-100%) rotateY(-180deg);

  .card__face--front {
    opacity: 10%;
  }
}

.card__face {
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: .2rem;
  overflow: hidden;
  // line-height: 260px;
  // text-align: center;
  // font-weight: bold;
  // font-size: 40px;
  backface-visibility: hidden;
  box-shadow: 1px 1px 2px 1px rgba(0, 0, 0, 0.1);
}

// .card__face--front {
//   background: red;
// }

.card__face--back {
  background: white;
  transform: rotateY(180deg);
}

.skill-item-container {
  position: relative;
  padding-left: 10px;
  display: flex;
  align-items: center;
  flex-direction: row;
  flex-wrap: wrap;
  cursor: pointer;
  background: white;

  &:hover {
    background: #ececec;
  }

  &:before {
    width: 6px;
    content: "";
    background: #6bd3ea;
    position:absolute;
    top:0;
    bottom:0;
    left:0;
  }

  .skill-type-container {
    display: flex;
    align-items: center;
    padding: 1rem .6rem;

    img {
      width: 70px;
      height: 70px;
      object-fit: contain;
    }

    .type-name {
      text-transform: capitalize;
      padding: 0 2rem;
    }
  }

  .percentage-container {
    width: 200px;
    height: 15px;
    border: 1px solid #e3e3e3;
    border-radius: .8rem;
    position: relative;
    overflow: hidden;

    .percentage {
      display: inline-block;
      height: 100%;
      transition: ease-in width 2s;
      animation: load 2s;
    }

    .hidden-percentage {
      display: inline-block;
      height: 100%;
      position: absolute;
      right: 0;
    }
  }
}

.text-container {
  background: white;
  width: 100%;
  height: 100%;
  padding: 1rem;
  box-sizing: border-box;

  a {
    color: #47c9e5;

    & + a, & + span {
      margin-left: .6rem;
    }
  }

  p {
    padding: .6rem 0;
  }
}

@keyframes load {
  0% {
    width: 0;
  }
  100% {
    width: 100%;
  }
}
</style>
