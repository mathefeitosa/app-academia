<template>
    <div class="card">
        <div class="card-body">
            <User />
            <hr>
            <div>
                <Button 
                :key="treino.id" 
                v-for="treino in treinos" 
                :text="treino.title"
                :treinoId="treino.id"
                @treino-selected="treinoSelector"/>
            </div>
            <hr>
            <Treino
            :treino="selectedTreino"/>
        </div>
    </div>
</template>

<script>
import Treino from './Treino'
import Button from './Button'
import User from './User'

export default {
    name: 'Treinos',
    components:{
        Treino,
        Button,
        User
    },
    props: {
        treinos: Array,
    },
    data(){
        return {
            selectedTreino: {}
        }
    },
    methods: {
        treinoSelector(id){
            this.selectedTreino = this.treinos[id-1]
        }
    },
    beforeMount(){
        this.treinoSelector(1)
    }
}
</script>