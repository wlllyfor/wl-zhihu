<template>
  <div>
    <div class="row">
      <div v-for="column in columnList" :key="column.id" class="col-4 mb-3">
        <div class="card h-100 shadow-sm">
          <div class="card-body text-center">
            <img class="rounded-circle w-25 my-3 border border-light" :src="column.avatar" :alt="column.title">
            <h5 class="card-title">{{column.title}}</h5>
            <p class="card-text text-left text-truncate">{{column.description}}</p>
            <a class="btn btn-outline-primary" href="#">进入专栏</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { computed, defineComponent, PropType } from 'vue'

export interface ColumnProps {
  id: number;
  title: string;
  avatar?: string;
  description: string;
}

export default defineComponent({
  name: 'ColumnList',
  props: {
    list: {
      type: Array as PropType<ColumnProps[]>,
      required: true
    }
  },
  setup (props) {
    const columnList = computed(() => {
      return props.list.map(column => {
        if (!column.avatar) {
          column.avatar = require('@/assets/cat.jpeg')
        }
        return column
      })
    })
    return {
      columnList
    }
  }
})
</script>

<style scoped>
</style>
