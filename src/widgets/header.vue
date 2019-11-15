<template>
  <div id="headeer">
      <b-container>
            <img id="logomain" src="@/assets/logo.png">
            <div id="logoname">
                <p>IDIOT MATRIX</p>
            </div>
            <div id="borderbottom"></div>
        </b-container>
  </div>
</template>
<script>
export default {
  methods: {
   
  }
};
</script>
<style scoped>
#logomain{
    position:absolute;
    left:4rem;
    top:2.5rem;
    height:3rem;
}
#logoname{
    height:3rem;
    width:5rem;
    position:absolute;
    left:7.3rem;
    text-align:left;
    top:2.6rem;
    font-family: Arial, Helvetica, sans-serif;
    font-weight:600;
    font-size:25px;
    line-height:1.5rem;
}
#borderbottom{
  border-bottom:1px solid white;
  position:absolute;
  left:2rem;
  right:2rem;
  top:6rem;
}
</style>