<template>
  <error-page
    :code="$route.params.type"
    :text="errorText[$route.params.type]"
  />
</template>

<script>
import ErrorPage from '@/components/ErrorPage'

export default {
  name: 'Error',
  components: {
    ErrorPage
  },
  data () {
    return {
      errorText: {
        403: '您无权访问该页面',
        404: '您访问的页面不存在',
        500: '服务器异常，请联系管理员'
      }
    }
  }
}
</script>
