<template>
  <ul class="navbar-nav mr-auto">
    <li class="nav-item">
      <router-link class="nav-link" to="/">Home</router-link>
    </li>
    <li class="nav-item">
      <router-link to="/gerentes" class="nav-link">
        Gerentes
      </router-link>
    </li>
        <li class="nav-item">
        <a
        href="#"
        class="nav-link"
        @click.prevent="efetuarLogout">Logout</a>
    </li>
    </ul>
</template>

<script>
import { logoutMixins } from '@/mixins'

export default {
  name: 'BarraNavegacaoQuandoLogado',
  mixins: [logoutMixins]
}
</script>

<style>

</style>