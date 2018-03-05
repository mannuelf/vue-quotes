<template>
    <div class="container is-fluid">
        <form action="">
            <div class="control">
                <label for="Quote">Quote</label>
                <text-area v-model="quote" class="textarea" placeholder="Enter a Quote" rows="5"></text-area>
            </div>
            <div class="control">
                <button @click.prevent="createNew" class="button is-primary"></button>
            </div>
        </form>
    </div>
</template>
<script>
export default {
  data() {
    return {
      quote: ""
    }
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote)
      this.quote = ""
    }
  },
  created() {
    console.log("Quote init");
  }
};
</script>
<style>

</style>
