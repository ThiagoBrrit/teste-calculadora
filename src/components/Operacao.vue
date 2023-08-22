<script setup>
    const props = defineProps(['operacao', 'num1', 'num2'])
</script>


<template>
    <div class="operation">
        <h2>Selecione a operação para o resultado</h2>
        <select @change="props.operacao">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
    </div>
    <div>
        <input @keyup="props.num1" required type="number" placeholder="Insira o número 1">
        <input @keyup="props.num2" required type="number" placeholder="Insira o número 2">
    </div>
</template>

<style scoped>

    h2{
        padding: 6px;
        margin-top: 24px;
    }
    input{
        margin: 30px;
        padding: 4px;
        border-radius: 10px;
        border: solid 3px #000;
    }
</style>