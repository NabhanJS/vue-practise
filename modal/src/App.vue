<template>
  <div id="app">
    <button class="btn" @click="showModal = true">
      Show Modal
    </button>
    <transition name="fade" appear="">
      <div class="modal-overlay" v-if="showModal" @click="showModal = false"> </div>
    
    </transition>

    <transition name="slide" appear="">
      <div class="modal" v-if="showModal">
        <h1>Hello Nabhan</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dolorum ducimus exercitationem eveniet aliquam, doloribus qui enim? Quisquam ad excepturi enim.
        </p>
        <button class="btn" @click="showModal = false">
           Hide Modal
        </button>
      </div>
        
    </transition>
    
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      showModal: true
    }
  },
 
  
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    
  }

  body{
    font-family: sans-serif;
  }

  #app{
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100vw;
    min-height: 100vh;
    overflow-x: hidden;
  }

  .btn{
    appearance: none;
    outline: none;
    border: none;
    background: none;
    cursor: pointer;
    display: inline-block;
    padding: 15px 25px;
    background-image: linear-gradient(to right, blue, yellow);
    border-radius: 10px;
    color: black;
    font-size: 20px;
    font-weight: bold;
    box-shadow: 2px 2px rgba(0, 0, 0, 0.5);
    transition: 0.5s ease-in-out;

  }

  .btn:hover{
    box-shadow: 4px 4px rgba(0, 0, 0, 0.8);
  }

  .modal-overlay{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 98;
    background-color: rgba(0, 0, 0, 0.4);
  }

  .modal{
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 99;
    width: 100%;
    max-width: 400px;
    background-color: white;
    border-radius: 16px;
    padding: 30px;

  }

  .modal h1{
    color: white;
    font-size: 32px;
    font-weight: bold;
    margin-bottom: 15px;

  }

  .modal p{
    color: blue;
    font-size: 20px;
    margin-bottom: 15px;
  }

  .fade-enter-active,
  .fade-leave-active{
    transition: opacity 1s;

  }

  .fade-enter,
  .fade-leave-to{
    opacity: 0;

  }

  .slide-enter-active,
  .slide-leave-active{
    transition: transform 1s;

  }

  .slide-enter,
  .slide-leave-to{
    transform: translateY(-50%) translateX(100vw) ;

  }





</style>
