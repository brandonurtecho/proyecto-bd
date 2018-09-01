<template>
    <div class="release">
        <div class="release__title">NEW PLAYSTATION 4 RELEASES</div>
        <div class="release__body">
            <div class="release__three">
                <div class="img__temporal">ss</div>
            </div>
            <div class="release__other">
                <div class="other__title">LANZAMIENTOS MAS RECIENTES</div>            
                <div class="other__container">
                    <div class="score">50</div>
                    <div class="title">Cualquier titulo de mierda</div>
                </div>
                <div class="other__container">
                    <div class="score">50</div>
                    <div class="title">Cualquier titulo de mierda</div>
                </div>
                <div class="other__container">
                    <div class="score">50</div>
                    <div class="title">Cualquier titulo de mierda</div>
                </div>
            </div>        
        </div>
    </div>
</template>

<script>
export default {
  name: "ReleaseSection",
  data() {
    return {};
  }
};
</script>


<style lang="scss">
.release {
  
  .release__title {
    background: #2e2e2e;
    color: white;
    font-weight: 800;
    font-size: 1.5em;
    padding: 10px;
  }
  .release__body {
    border: solid 1px #ccc;
    border-top: none;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    .release__three{

    }
    .release__other {
      .other__title {
        font-weight: 800;
        color: #2e2e2e;
      }
      .other__container {
        margin-top: 10px;
        display: flex;
        align-items: center;
        .score {
          width: 30px;
          height: 30px;
          padding: 6px;
          color: white;
          font-size: 1em;
          font-weight: 800;
          background: #6c3;
          cursor: pointer;
        }
        .title {
          color: #2e2e2e;
          font-size: .8em;
          font-weight: 700;
          cursor: pointer;
          padding: 10px;
        }
      }
    }
  }
}
</style>
