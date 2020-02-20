<template>
  <div class="col-sm-6 col-md4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        {{ quote }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['quote']
}
</script>

<style>
.panel-body {
  font-family: "Arizonia", cursive;
  font-size: 2rem;
}

.quote {
  cursor: pointer;
}
.quote:hover {
  background-color: #ffe2e2;
}
</style>
