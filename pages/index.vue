<template>
  <div class="mt-2">
    <v-row justify="center" align="center" class="pt-5" >
      <v-col cols="12" sm="8" md="7">
        <span class="d-flex justify-center align-center mb-10">
          <h1 class="primary--text pr-2">CSS</h1><h1>GENERATOR</h1>
        </span>
        <p style="    text-align: center;">
          Prosty generator, za pomocą którego dobierzesz odpowiednie wartości
          dla wybranych właściwości CSS. Wygodne dostosowanie parametrów za
          pomocą suwaków, podgląd na żywo i błyskawiczne kopiowanie gotowego
          kodu CSS.
        </p>
      </v-col>
    </v-row>
    
    <div style="width: 60%; margin-left: 210px;">
    <v-row class="" >
      <v-col  v-for="x in items" cols="4" sm="12" md="4">
        <v-hover v-slot="{ hover }" open-delay="200">
       
        <v-btn :class="{ 'primary button-color': hover }" :to="x.to"  class="button" outlined color="blue lighten-1"> {{x.name}} </v-btn>

      </v-hover>
      </v-col>
    </v-row>
  </div>
</div>
</template>
<style>
.button-color :hover{
  color: black;
}
.button{
  border: 2px solid #5983fc;
    border-radius: 4px;
    display: inline-block;
    padding: 25px !important;
    width: 200px;
    height: 69px !important;
}
</style>
<script>
export default {
  name: "IndexPage",
  data() {
    return {

      items: [
        {
          name: "Box shadow",
          title: "Welcome",
          to: "/box",
        },
        {
          name: "Text shadow",
          title: "Welcome",
          to: "/Text",
        },
        {
          name: "Flexbox",
          title: "Welcome",
          to: "/Flexbox",
        },
        {
          name: "Border radius",
          title: "Welcome",
          to: "/Border",
        },
        {
          name: "Button",
          title: "Welcome",
          to: "/Button",
        },
        {
          name: "Gradient",
          title: "Welcome",
          to: "/Gradient",
        },
        {
          name: "Transition",
          title: "Welcome",
          to: "/Transition",
        },
        {
          name: "Transform",
          title: "Inspire",
          to: "/Transform",
        },
        {
          name: "Background",
          title: "Inspire",
          to: "/Background",
        },
      ],
    };
  },
};

</script>
