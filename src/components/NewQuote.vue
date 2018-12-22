<template>
  <div class="row">
    <form>
      <div class="col-md-8 offset-sm-2 col-12 col-lg-6 offset-md-3 form-group">
        <label>Quote</label>
        <textarea class="form-control" rows="5" cols="80" v-model="quote"></textarea>
      </div>
      <div class="col-md-8 offset-sm-2 col-12 col-lg-6 offset-md-3 form-group">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      this.$emit("quoteAdded", this.quote);
      this.quote = "";
    }
  }
};
</script>

<style>
</style>