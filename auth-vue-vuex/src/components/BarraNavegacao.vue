<template>
   <nav class="navbar navbar-expand-lg navbar-bytebank">
      <a class="navbar-brand" href="#">ByteBank</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <BarraNavegacaoQuandoLogado v-if="usuarioestaLogado" />
        <BarraNavegacaoQuandoDeslogado v-else />
      </div>
    </nav>
</template>

<script>
import BarraNavegacaoQuandoLogado from './BarraNavegacaoQuandoLogado.vue'
import BarraNavegacaoQuandoDeslogado from './BarraNavegacaoQuandoDeslogado.vue'
export default {
  name: 'BarraNavegacao',
  components: {
    BarraNavegacaoQuandoLogado,
    BarraNavegacaoQuandoDeslogado
  },
  computed: {
    usuarioestaLogado() {
      console.log(Boolean(localStorage.getItem('token')))
      return Boolean(localStorage.getItem('token'));
    }
  }
}
</script>

<style>

</style>