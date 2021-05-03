<template>
  <article class="column is-9 is-offset-1 message is-info">
      <div class="message-header is-warning">Marcos 11:25-26</div>
  <div class="message-body verse-body"> {{versiculo}} </div>
</article>
</template>

<script> 
import axios from 'axios';

export default{
    data(){
        return{
            versiculo: ""
        }
    },
    created: async function(){
        this.versiculo = "E, quando estiverem orando, se tiverem alguma coisa contra alguém, perdoem-no, para que também o Pai celestial perdoe os seus pecados. Mas, se vocês não perdoarem, também o seu Pai que está nos céus não perdoará os seus pecados"
        try{
            const res = await axios.get("https://www.bibliaon.com/versiculo_do_dia");
            console.log(res);
        } catch(error) {
            console.log(error);
        }

    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Pangolin&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Montserrat&family=Pangolin&display=swap');

.verse-title{
    font-family: 'Pangolin', sans-serif;
}

.verse-body{
    font-family: 'Montserrat', sans-serif;
}
</style>