<template>
  <div class="container-sm">
    <Treinos :treinos="treinos" />
  </div>
</template>

<script>
import Treinos from './components/Treinos'

export default {
  name: 'App',
  components: {
    Treinos,
  },
  data(){
    return {
      treinos: []
    }
  },
  created(){
    this.treinos = [
      {
        id: 1,
        title: 'Treino A',
        exercises: [
          'Remada Peito',
          'Supino Reto',
          'Puxada Máquina'
        ]
      },
      {
        id: 2,
        title: 'Treino B',
        exercises: [
          'Levantamento Terra',
          'Leg Press 90°',
          'Agachamento'
        ]
      },
      {
        id: 3,
        title: 'Treino C',
        exercises: [
          'Sholder Press',
          'Abdução Lateral',
          'Remada Alta na Polia'
        ]
      }
    ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
