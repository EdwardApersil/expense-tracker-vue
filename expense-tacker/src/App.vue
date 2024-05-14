<script setup>
import Header from './components/Header.vue';
import Balance from './components/Balance.vue';
import IncomeExpense from './components/IncomeExpense.vue';
import TransactionsList from './components/TransactionsList.vue';
import AddTransactions from './components/AddTransactions.vue';
import { ref } from 'vue';


const trans = ref([
  { id: "1", name: "Food", money: "-500" },
  { id: "2", name: "Car", money: "500" },
  { id: "3", name: "Paycheck", money: "500" },
  { id: "4", name: "Grocery", money: "-500" },
])


</script>

<template>
  <Header />
  <div class="container">
    <Balance />
    <IncomeExpense :trans="tans"/>
    <TransactionsList :trans="trans"/>
    <AddTransactions />
  </div>
</template>
