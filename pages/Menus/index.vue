<template>
  <div>
    <Receipt
      v-for="receipt in receipts"
      :key="receipt.idMeal"
      :idMeal="receipt.idMeal"
      :receipt="receipt.receipt"
    />
  </div>
</template>
<script>
import axios from 'axios'
import Receipt from '../../components/Receipt'
export default {
  components: {
    Receipt,
  },
  data() {
    return {
      meals: [],
    }
  },
  async created() {
    const res = await axios.get(
      'https://www.themealdb.com/api/json/v1/1/search.php?s=Arrabiata'
    )
    this.meals = res.data.results
  },

  head() {
    return {
      title: "Today's Menu",
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Enjoy your menu!',
        },
      ],
    }
  },
}
</script>
<style scoped></style>
