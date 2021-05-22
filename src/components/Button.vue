<template>
    <button 
        class="btn btn-dark"
        @click="onClick" >
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        treinoId: {
            type: Number,
            default: 1
        }
    },
    methods: {
        onClick(){
            this.$emit('treino-selected', this.treinoId)
        }
    }
}
</script>