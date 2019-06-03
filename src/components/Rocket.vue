<template>
  <div class="card col-4">
    <img :src="rocket.image" class="card-img-top rocket-image" alt="...">
    <div class="card-body">
      <h5 class="card-title">{{rocket.name}}</h5>
      <p class="card-text">{{rocket.description}}</p>
      <button @click="removeRocket(rocket)" class="btn btn-primary">Delete</button>
    </div>
  </div>
</template>

<script>
import { mapMutations } from "vuex";
export default {
  props: ["rocket"],
  methods: mapMutations(['removeRocket'])
};
</script>

<style media="screen">
.rocket-image {
  max-height: 400px;
  width: auto;
}
</style>