
<script setup>
    const props = defineProps (['cadastraTarefa', 'tarefaTemp', 'trocarFiltro', 'editaTarefaTemp'])
</script>



<template>
    <form  @submit.prevent="props.cadastraTarefa">
    <div class="row">
    <div class="col">
    <input class="form-control" :value="props.tarefaTemp" @change="props.editaTarefaTemp" placeholder="Digite aqui a descrição da tarefa" required>
    </div>
    <div class="col-md-2">
    <button class="btn btn-primary" type="submit">Cadastrar</button>
    </div>
    <div class="col-md-2">
    <select @change="props.trocarFiltro" class="form-control">
        <option value="todas">Todas as Tarefas</option>
        <option value="pendentes">Pendente</option>
        <option value="finalizadas">Finalizadas</option>
    </select>
    </div>
    </div>
    </form>
</template>