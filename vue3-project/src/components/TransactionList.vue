<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li
      v-for="transaction in transactions"
      v-bind:key="transaction.id"
      :class="transaction.amount < 0 ? 'minus' : 'plus'"
    >
      {{ transaction.text }} <span>${{ transaction.amount }}</span>
      <button class="delete-btn">x</button>
    </li>
    <!-- <li class="minus">
      Gas Bill <span>$400</span>
      <button class="delete-btn">x</button>
    </li>

    <li class="plus">
      Paycheck <span>$400</span>
      <button class="delete-btn">x</button>
    </li> -->
  </ul>
</template>

<script>
export default {
  data() {
    return {
      transactions: [
        { id: 1, text: "Flower", amount: -19.99 },
        { id: 2, text: "Salary", amount: 219.99 },
        { id: 3, text: "Book Purchase", amount: -10.99 },
      ],
    };
  },
};
</script>
