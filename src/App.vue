<template>
  <b-container class="center">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div class="tarefas">
    <div>
      <h2>Tarefas</h2>
    </div>
    <b-card-group deck v-for="item in lista" v-bind:key="item.id" class="margin">
      <b-card v-if="item.estaCompleta" border-variant="primary" :header="item.descricao" header-bg-variant="primary" header-text-variant="white" align="center">
        <b-card-text>Completo</b-card-text>
      </b-card>
      <b-card v-else border-variant="danger" :header="item.descricao" header-bg-variant="danger" header-text-variant="white" align="center">
        <b-card-text>Incompleto</b-card-text>
      </b-card>
    </b-card-group>
  </div>
  </b-container>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  name: 'App',
  components: {
    // HelloWorld
  },data: function(){
    return{
      lista:[
        {id: 0, descricao: "Jogar", estaCompleta:  false},
        {id: 1, descricao: "Fazer live", estaCompleta:  false},
        {id: 2, descricao: "Estudar", estaCompleta:  true},
        {id: 3, descricao: "Fazer o tp1", estaCompleta:  true},
        {id: 4, descricao: "Limpar a casa", estaCompleta:  false}
      ],
    }
  },
}
</script>

<style>
.center{
  text-align: center;
}
.margin{
  margin-top: 20px;
}

</style>
