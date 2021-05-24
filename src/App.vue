<template>
  <div id="app">
    <header>
    <h1>My personal cost</h1>
    </header>
    <main>
      <button @click="show=!show">NEW COST +</button>
      <PaymentsForm v-if="show" @add="onDataAdded"/>
      <PaymentsList :items="paymentsList"/>
    </main>
  </div>
</template>

<script>
import PaymentsList from './components/PaymentsList.vue'
import PaymentsForm from './components/PaymentsForm.vue'
export default {
  name: 'App',
  components: {
    PaymentsList,
    PaymentsForm
  },
  data () {
    return {
      show: false,
      paymentsList: [
        {
        date:'13.05.2021',
        category: 'education',
        price: 521
      },
      {
        date:'12.05.2021',
        category: 'education',
        price: 680
      },
      {
        date:'11.05.2021',
        category: 'education',
        price: 1460
      },
      {
        date:'10.05.2021',
        category: 'education',
        price: 7852
      }
      ]
    }
  },
  methods: {
        onDataAdded(data){
          this.paymentsList.push(data)
        },
  }
}
</script>

<style lang="scss">
</style>
