<template>
    <div class="componente">
        <h2>Alterar os Dados de Usuário</h2>
        <p>Edite as informações</p>
        <p>Idade do usuario: <strong>{{idade}}</strong></p>
        <button @click="alterarIdade">Alterar idade</button>
    </div>
</template>

<script>
import barramento from "../barramento";
export default {
  props: {
    idade: {
      type: Number,
      default: undefined,
    },
  },
  methods: {
    alterarIdade() {
      this.idade = 33;
      barramento.$emit("idadeMudou", this.idade);
    },
  },
};
</script>

<style scoped>
.componente {
  flex: 1;
  background-color: #98b99a;
  color: #fff;
}
</style>
