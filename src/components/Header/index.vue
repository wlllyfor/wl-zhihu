<template>
  <div class="mb-2">
    <nav class="navbar navbar-dark bg-primary pl-4 rounded-sm">
      <a class="navbar-brand" href="#">知乎专栏</a>
      <ul v-if="!user.isLogin" class="mr-3">
        <li class="list-inline-item">
          <a href="#" class="btn btn-outline-light my-2">注册</a>
        </li>
        <li class="list-inline-item">
          <a href="#" class="btn btn-outline-light my-2">登录</a>
        </li>
      </ul>
      <div v-else class="mr-3 dropdown">
        <button type="button" class="btn btn-light dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
          欢迎你，{{user.name}}
        </button>
      </div>
    </nav>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export interface HeaderProps {
  id: number;
  name?: string;
  isLogin: boolean;
}

export default defineComponent({
  name: 'Header',
  props: {
    user: {
      type: Object as PropType<HeaderProps>,
      required: true
    }
  }
})
</script>

<style scoped>
</style>
