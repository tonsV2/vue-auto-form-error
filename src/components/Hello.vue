<template>
  <div class="hello">
    <auto-form :schema="schema" :model="model" @submit="onSubmit"></auto-form>
  </div>
</template>

<script>
import AutoForm from 'vue-auto-form'

export default {
  components: {
    AutoForm
  },
  data () {
    return {
      schema: {
        title: {
          type: String,
          label: 'Title',
          max: 50
        },
        author: {
          type: String,
          label: 'Author'
        }
      },
      model: {}
    }
  },
  methods: {
    onSubmit () {
      console.log(this.model)
    }
  }
}
</script>
