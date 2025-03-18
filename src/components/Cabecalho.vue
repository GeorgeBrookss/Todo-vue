<script setup>
    const props = defineProps(['tarefasPendentes'])
</script>

<template>
    <div class="container">
    <header class="p-5 mt-4 mt-4 bg-light rounded-3">
    <h1>Minhas Tarefas</h1>
    <p>
        Você possui {{ props.tarefasPendentes }} tarefas pendentes
    </p>
    </header>
    </div>
</template>