<template>
 <section>
     
      <h1>List of dogs</h1>
  <b-table striped hover :items="items"></b-table>
 </section>
</template>

<script>
const items = [
  { id: 1, name: 'dog1', race: 'race1', birthdate: '1980/08/08' },
  { id: 2, name: 'dog2', race: 'race2', birthdate: '1980/09/08' },
  
]

export default {
  data () {
    return {
      items: items
    }
  }
}
</script>