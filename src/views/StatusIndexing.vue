<template>
  <div>
    <router-link to="/">Back</router-link>
    <div>
      Index status
    </div>
    <CodeBlock>
      {{ formattedStatus }}
    </CodeBlock>
  </div>
</template>

<script>
import CodeBlock from "@/ui/CodeBlock"

export default {
  components: {
    CodeBlock,
  },
  computed: {
    formattedStatus () {
      return JSON.stringify(this.$store.state.status, null, 2)
    },
  },
}
</script>

<style scoped>
</style>
