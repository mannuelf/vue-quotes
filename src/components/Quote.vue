<template>
    <div class="container is-fluid">
        <div class="card">
           <p>HELLO</p>
        </div>
    </div>
</template>
<script>
export default {
  name: 'Quote',
  props: ["quotes"],
  created() {
    console.log("Quote Init");
  }
}
</script>
<style>

</style>
