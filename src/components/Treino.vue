<template>
    <div class="card">
        <h5 class="card-header bg-danger text-light">{{ treino.title }}</h5>
        <ol class="list-group  list-group-numbered">
            <li 
            class="list-group-item text-start"
            v-for="exercise in treino.exercises">{{exercise}}</li>
        </ol>
    </div>
</template>

<script>
export default {
    name: 'Treino',
    props: {
        treino: Object,
    }
}
</script>