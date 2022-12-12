<template>
  <div class="">
  
    <v-row style="background-color: white" class="p">
   
      <v-col cols="3" class="primary--text me-16" style="background-color: white;box-shadow: 1px 1px 1px 1px whitesmoke; ">
        CSS box-shadow
        <br />
        <div class="d-flex">
          <p>{{ ex1.label }}</p>
          <span class="ps-16 ms-16">{{ ex1.val }}</span>
        </div>
        <v-slider v-model="ex1.val" max="100" min="-100"></v-slider>
        <div class="d-flex">
          <p>{{ ex2.label }}</p>
          <span class="ps-16 ms-16">{{ ex2.val }}</span>
        </div>
        <v-slider v-model="ex2.val" max="100" min="-100"></v-slider>
        <div class="d-flex">
          <p>{{ ex3.label }}</p>
          <span class="ps-16 ms-16">{{ ex3.val }}</span>
        </div>
        <v-slider v-model="ex3.val" max="100" min="-100"></v-slider>
        <div class="d-flex">
          <p>{{ ex4.label }}</p>
          <span class="ps-16 ms-16">{{ ex4.val }}</span>
        </div>
        <v-slider v-model="ex4.val" max="100" min="-100"></v-slider>
        <div class="d-flex">
          <p>{{ ex5.label }}</p>
          <span class="ps-16 ms-16">{{ ex5.val }}</span>
        </div>
        <v-slider v-model="ex5.val" max="100" min="-100"></v-slider>
      </v-col>
      <v-col justify="center" align="center" class="pt-15 mt-15">
        <v-hover>
          <template>
            <!-- :elevation="hover ? ex1.val : ex1.val" -->
            <!-- :elevation="hover ? 10 : ex3.val" class="" -->
            <div
              class="shadow"
              :style="{ 'box-shadow': ex1.val * ex1.val + `px  ${ex2.val}px ${ex3.val}px ${ex4.val}px #42445A ` }"
            ></div>
          </template>
        </v-hover>
      </v-col>
    </v-row>
    <!-- Using the elevation prop -->
  </div>
</template>
<style>
.shadow {
  width: 250px;
  height: 250px;
  background-color: rgb(237, 239, 239);
}
</style>
<script>
export default {
  data() {
    return {
      x: 5,
      color: "red",
      ex1: { label: "Horizontal", val: 25, color: "orange darken-3" },
      ex2: { label: "Vertical", val: 75, color: "green lighten-1" },
      ex3: { label: "Blur", val: 50, color: "red" },
      ex4: { label: "Spread", val: 50, color: "red" },
      ex5: { label: "Kolor", val: 50, color: "red" },
    };
  },
};
</script>
