<template>
  <div id="app">
    <div class="container">
      <div class="user-input">
        <div class="input-wrapper">
          <label for="first-name">First Name*</label>
          <input id="first-name" type="text" v-model="firstName" placeholder="First name here">
        </div>
        <div class="input-wrapper">
          <label for="last-name">Last Name*</label>
          <input id="last-name" type="text" v-model="lastName" placeholder="Last name here">
        </div>
        <div class="input-wrapper">
          <label for="prefer-framework">JS Framework*</label>
          <input id="prefer-framework" type="text" v-model="jsPreferFw" placeholder="JS favourite framework">
        </div>
      </div>
      <Cover
        :firstName="firstName"
        :lastName="lastName"
        :jsPreferFw="jsPreferFw"
      />
    </div>
    <div class="change-me">
      *Feel free to change input data
    </div>
  </div>
</template>

<script>
import Cover from './components/Cover.vue'

export default {
  name: 'App',
  components: {
    Cover
  },
  data() {
    return {
      firstName: 'Fabio',
      lastName: 'Mezzina',
      jsPreferFw: 'Vue.js'
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  position: relative;
  min-height: 100vh;
  min-height: 100vh;
  font-family: 'Courier New', Courier, monospace;
  color: #fff;
  background-image: linear-gradient(180deg,rgba(83,47,248,.82),#4c1ff2);
  .container {
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    padding: 0 2em;
    max-width: 1200px;
    min-height: 100%;
    // user input
    .user-input {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
      min-height: 25vh;
      margin: 1em 0;
      .input-wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        flex-basis: calc(100% / 3);
        margin: auto 0;
        padding: 1em;
        label {
          font-size: 1.1rem;
          font-weight: 600;
          margin-bottom: .5em;
          letter-spacing: .1em;
          color: rgb(255, 186, 0);
        }
        input {
          padding: .8em;
          font-size: 1.2rem;
          text-align: center;
          color: #ff7575;
          background: transparent;
          border: 2px solid rgba(255, 255, 255, .4);
          border-radius: 1.6em;
          outline: none;
          &:focus {
            background-color: rgba(255, 255, 255, .05);
          }
        }
      }
    }
  }

  // welcome modal
  .change-me {
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    padding: .3em .5em;
    color: rgb(255, 186, 0);
    background-color: rgba(0, 0, 0, .4);
    border-bottom-left-radius: .7em;
    z-index: 1;
  }
}
</style>