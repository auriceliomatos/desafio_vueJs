<script setup>
import { computed, ref } from "vue";
import foot from './components/foot.vue';


// Declaração de variáveis reativas
const num1 = ref(0);
const num2 = ref(0);
const operation = ref("+");

// Computação do resultado
const result = computed(() => {
  switch (operation.value) {
    case "+":
      return num1.value + num2.value;
    case "-":
      return num1.value - num2.value;
    case "*":
      return num1.value * num2.value;
    case "/":
      return num2.value !== 0 ? num1.value / num2.value : "Erro: Divisão por zero";
    default:
      return "Operação inválida";
  }
});
</script>

<!-------------------------------------- template --------------------------------->

<template>
  <div id="app" class="container">
  <h1>Calculadora do Automatica</h1>

    <img src="@/assets/r-1.jpg" alt="Robô Infantil" class="robot-image" />
    
    <div class="calculator">
      <input
        type="number"
        v-model.number="num1"
        placeholder="Digite o primeiro número"
      />
      <select v-model="operation">
        <option value="+">Somar (+)</option>
        <option value="-">Subtrair (-)</option>
        <option value="*">Multiplicar (*)</option>
        <option value="/">Dividir (/)</option>
      </select>
      <input
        type="number"
        v-model.number="num2"
        placeholder="Digite o segundo número"
      />
      <p class="result">Resultado: {{ result }}</p>
         <foot />
    </div>
  </div>
</template>

<!--------------------------------------- style ---------------------------------------->

<style scoped>

.container {
  max-width: 500px;

  padding: 10px;
  text-align: center;
  background-color: #f9f9f9;
  border: 2px solid #e0e0e0;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
  display: flex;

}
.robot-image {
  width: 200px;
  margin: 0px;
  padding: 10px;
  
  
}

.calculator {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

input,
select {
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

input:focus,
select:focus {
  outline: none;
  border-color: #007bff;
  box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
}

.result {
  margin-top: 20px;
  font-size: 18px;
  font-weight: bold;
  color: #007bff;
}

h1 {
  font-size: 24px;
  color: #333;
  margin-bottom: 20px;
}
</style>