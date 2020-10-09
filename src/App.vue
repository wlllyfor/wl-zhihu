<template>
  <div class="container">
    <column-list :list="list" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList/index.vue'

const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'wanglin',
    // avatar: '',
    description: 'a  happpy boy'
  },
  {
    id: 2,
    title: 'wanglin1',
    avatar: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1602234246222&di=b5211ad788a14db8c16e011846952998&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201509%2F16%2F20150916235818_HVAk2.jpeg',
    description: 'a  sad boy'
  },
  {
    id: 2,
    title: 'wanglin1',
    avatar: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1602234246222&di=b5211ad788a14db8c16e011846952998&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201509%2F16%2F20150916235818_HVAk2.jpeg',
    description: 'a  sad boy'
  },
  {
    id: 2,
    title: 'wanglin1',
    avatar: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1602234246222&di=b5211ad788a14db8c16e011846952998&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201509%2F16%2F20150916235818_HVAk2.jpeg',
    description: 'a  sad boy'
  },
  {
    id: 2,
    title: 'wanglin1',
    avatar: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1602234246222&di=b5211ad788a14db8c16e011846952998&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201509%2F16%2F20150916235818_HVAk2.jpeg',
    description: 'a  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boya  sad boy'
  },
  {
    id: 2,
    title: 'wanglin1',
    avatar: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1602234246222&di=b5211ad788a14db8c16e011846952998&imgtype=0&src=http%3A%2F%2Fb-ssl.duitang.com%2Fuploads%2Fitem%2F201509%2F16%2F20150916235818_HVAk2.jpeg',
    description: 'a  sad boy'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList
  },
  setup () {
    return {
      list: testData
    }
  }
})
</script>

<style>
</style>
