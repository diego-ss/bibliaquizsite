<template>
  <nav class="navbar navbar-background" role="navigation" aria-label="main navigation">
  <div class="navbar-brand navbar-background">
    <a class="navbar-item" href="/">
      <img src="../assets/PixelBible.png" width="32" height="32">
      <label class="title-text">BibliaQuizApp</label>
    </a>

    <a role="button" class="navbar-burger navbar-item-icon" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu navbar-background">
    <div class="navbar-start">


      <a class="navbar-item navbar-background" href="#home-div">
        <i class="fas fa-info-circle navbar-item-icon"></i>
        <p class="navbar-item-text">sobre</p>
      </a>

        <a class="navbar-item navbar-background" href="#contact-form">
        <i class="fas fa-envelope navbar-item-icon"></i>
        <p class="navbar-item-text">contato</p>
      </a>

    <a class="navbar-item navbar-background" href="#versiculo-div">
        <i class="fas fa-pray navbar-item-icon"></i>
        <p class="navbar-item-text">versículo do dia</p>
    </a>
      
    </div>

    <div class="navbar-end navbar-background">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-regular" href="https://play.google.com/store/apps/details?id=br.com.diegoss.bibliaquizapp">
            <strong>baixe agora!</strong>
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<script>
document.addEventListener('DOMContentLoaded', () => {

  // Get all "navbar-burger" elements
  const $navbarBurgers = Array.prototype.slice.call(document.querySelectorAll('.navbar-burger'), 0);

  // Check if there are any navbar burgers
  if ($navbarBurgers.length > 0) {

    // Add a click event on each of them
    $navbarBurgers.forEach( el => {
      el.addEventListener('click', () => {

        // Get the target from the "data-target" attribute
        const target = el.dataset.target;
        const $target = document.getElementById(target);

        // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
        el.classList.toggle('is-active');
        $target.classList.toggle('is-active');

      });
    });
  }
});

window.onload = (function() {

  // Check for click events on the navbar burger icon
  document.querySelector(".navbar-burger").click(function() {

      // Toggle the "is-active" class on both the "navbar-burger" and the "navbar-menu"
      document.querySelector(".navbar-burger").toggleClass("is-active");
      document.querySelector(".navbar-menu").toggleClass("is-active");

  });
});
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Pangolin&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat&family=Pangolin&display=swap');

.title-text{
    font-family: 'Montserrat', sans-serif;
    margin-left: 5%;
    margin-right: 0;
    padding: 0;
    font-size: 23px;
    color: whitesmoke;
}

.navbar-item-text{
    font-family: 'Montserrat', sans-serif;
    margin-left: 5px;
    margin-top: 1px;
    color: whitesmoke;
}

.navbar-item-icon{
    color: whitesmoke;
}

.navbar-item:hover{
  background-color: #038593;
}

.navbar-background{
    background-color: #00B3C6;
    color: #00B3C6;
}
</style>