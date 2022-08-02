<template>
  <form v-on:submit.prevent="login">
    <button type="submit">
      Login
    </button>
  </form>
</template>

<script>
import {useStore} from 'vuex'

export default {
  setup() {
    const store = useStore()

    const login = () => {
      store.dispatch('login', {
        email: 'unbsold@yandex.ru',
        password: '12345678'
      })
    }

    return {
      login
    }
  }
}
</script>