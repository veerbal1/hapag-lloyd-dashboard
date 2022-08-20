<template>
  <div id="main">
    <div id="content">
      <section id="left">
        <div id="left-content">
          <div id="left-content-header">
            <img src="../../assets/images/logo.png" alt="">
          </div>
          <div id="left-content-body">
            <p>
              <!-- Container shipping company. It drive world economy-->
              We <span>drive</span><br/> world's <span>economy.</span>
            </p>
          </div>
        </div>
      </section>
      <section id="right"></section>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
#main {
  width: 100vw;
  height: 100vh;
  background-image: url('../../assets/images/bg2.jpeg');
  background-position: top;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  background-repeat: no-repeat;

  #content {
    width: 70%;
    height: 60%;
    background-color: transparent;
    max-width: 1007px;
    max-height: 425px;
    display: flex;

    section {
      flex: 1;
      height: 100%;

      &#left {
        display: flex;
        align-items: center;

        #left-content {
          #left-content-header {
            position: relative;
            right: 6%;
          }

          #left-content-body {
            p {
              text-transform: uppercase;
              color: var(--gray);
              font-size: 2em;
              line-height: initial;

              span {
                font-size: 3rem;
                font-weight: bolder;
                color: var(--secondary)
              }
            }
          }
        }
      }
    }
  }
}
</style>