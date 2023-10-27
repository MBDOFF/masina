<script setup>

const masina = ref({marginLeft: "0px", marginTop: "0px"});

function press(e){
  console.log(e);
  const left = parseInt(masina.value.marginLeft.slice(0, -2));
  const top = parseInt(masina.value.marginTop.slice(0, -1));
  if(e.key === "a"){
    masina.value.marginLeft = left - 20 + "px";
  }else if(e.key==="d"){
    masina.value.marginLeft = left + 20 + "px";
  }else if(e.key === "w"){
    masina.value.marginTop = top - 20 + "px";
  }else if(e.key === "s"){
    masina.value.marginTop = top + 20 + "px";
  }
}

</script>

<template>
  <input @keyup="press" />
  <div>
    <img :style="masina" src="https://imgd.aeplcdn.com/370x208/n/cw/ec/141867/nexon-exterior-right-front-three-quarter-71.jpeg?isig=0&q=80" />
  </div>
</template>
