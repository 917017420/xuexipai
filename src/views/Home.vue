<template>
<div style="height: 100%">
  <header class="hero hero--map gps-bg">

    <div class="gps-bg__guts">
      <div class="gps-bg__bg"></div>
      <div class="gps-bg__route"></div>
      <div class="gps-bg__marker"></div>
    </div>
    <div class="gps-bg__fade"></div>

    <div class="hero__title">
      qwdqw
    </div>

  </header>
</div>
</template>

<script>
export default {
  name: 'Home',
  components: {}
}

</script>
<style scoped>
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    -webkit-transition: all 0.25s cubic-bezier(0.37, 0, 0.45, 0.99);
    transition: all 0.25s cubic-bezier(0.37, 0, 0.45, 0.99);
  }
  *:before, *:after {
    box-sizing: inherit;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Fira Sans", "Helvetica Neue", sans-serif;
    line-height: 1.75;
    background-color: #fafafa;
  }

  @-webkit-keyframes driving {
    0% {
      -webkit-transform: translateY(-480px);
      transform: translateY(-480px);
    }
    100% {
      -webkit-transform: translateY(0);
      transform: translateY(0);
    }
  }

  @keyframes driving {
    0% {
      -webkit-transform: translateY(-480px);
      transform: translateY(-480px);
    }
    100% {
      -webkit-transform: translateY(0);
      transform: translateY(0);
    }
  }
  .hero__title {
    padding: 3em 2rem 16rem;
    text-align: center;
    color: #080314;
    position: relative;
    z-index: 0001;
    top: 243px;
  }

  .gps-bg {
    background-color: rgba(34, 167, 245, 0.39);
    position: relative;
    -webkit-perspective: 500px;
    perspective: 500px;
    overflow: hidden;
    height: 760px;
  }
  .gps-bg:after {
    content: '';
    background-color: #fafafa;
    position: absolute;
    width: 200%;
    height: 5em;
    bottom: 0;
    -webkit-transform: skewY(-2deg);
    transform: skewY(-2deg);
  }
  .gps-bg__guts {
    position: absolute;
    -webkit-transform: rotateX(45deg);
    transform: rotateX(45deg);
    width: calc(100% + 1000px);
    height: 100%;
    left: -500px;
  }
  .gps-bg__bg {
    height: 1300px;
    background-image: url(../assets/roads.svg);
    background-position: 50%;
    background-size: 25%;
    position: absolute;
    top: -162px;
    width: 100%;
    -webkit-transform: translateY(-650px);
    transform: translateY(-650px);
    -webkit-animation: driving 10000ms linear 0ms infinite;
    animation: driving 10000ms linear 0ms infinite;
  }
  .gps-bg__route {
    width: 2em;
    background-color: #fff;
    position: absolute;
    top: -162px;
    bottom: -162px;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
    box-shadow: 0 0 13px 5px rgba(46, 18, 107, 0.25);
  }
  .gps-bg__route:after {
    content: '';
    width: 60%;
    background-color: #6c38de;
    position: absolute;
    top: 0;
    bottom: 35%;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
  }
  .gps-bg__fade {
    background-image: -webkit-linear-gradient(top, #ac8dff 10%, rgba(172, 141, 255, 0) 100%);
    background-image: linear-gradient(to bottom, #ac8dff 10%, rgba(172, 141, 255, 0) 100%);
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 60%;
    z-index: 1;
  }
  .gps-bg__marker {
    height: 6em;
    width: 6em;
    background-color: #fff;
    border-right: 1px solid #ddd;
    border-bottom: 3px solid #ddd;
    border-left: 1px solid #ddd;
    border-radius: 100%;
    position: absolute;
    top: 60%;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
    box-shadow: 0 0.125em 10px 3px rgba(46, 18, 107, 0.25);
  }
  .gps-bg__marker:after {
    content: '';
    border-left: 1.5em solid transparent;
    border-right: 1.5em solid transparent;
    border-bottom: 3em solid #6c38de;
    position: absolute;
    top: 20%;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
  }
</style>
