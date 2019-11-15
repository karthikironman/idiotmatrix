<template>
  <div id="contentbar">
    <p class="topname">CONTENT</p>
    <b-container v-for="(item,index) in text" :key="index">
      <b-row>
        <b-col cols="2" class="settingbtn">
          <font-awesome-icon icon="align-justify" />
        </b-col>
        <b-col cols="8">
          <b-form-textarea>
            style="overflow:hidden"
            id="textarea"
            v-model="message"
            placeholder="Enter something..."
            rows="3"
            max-rows="12"
          ></b-form-textarea>
        </b-col>
        <b-col cols="2" class="deletebtn" @click="deleteit(index)">
          <font-awesome-icon icon="trash-alt" />
        </b-col>
      </b-row>
      <b-row class="mx-auto arrowdown" @click="btb=!btb">
        <font-awesome-icon icon="arrow-down" />
        <font-awesome-icon v-if="btb" class="btback" icon="sync-alt" />
      </b-row>
    </b-container>
    <b-button variant="outline-primary" class="botton" @click="addInput()">+</b-button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      text: [""],
      message: "",
      btb: false
    };
  },
  methods: {
    addInput() {
      this.text.push("");
    },
    deleteit(val) {
      this.text.splice(val, 1);
    }
  }
};
</script>
<style scoped>
.btback {
  position: absolute;
  left: 12rem;
  margin-top: 0.2rem;
}
.arrowdown {
  display: block;
  width: 2rem;
  padding: 0.5rem;
}
.deletebtn {
  color: red;
  padding-left: 0;
  margin: auto;
}
.settingbtn{
 position:relative;
 left:1.6rem;

  margin: auto;
}
#contentbar {
  position: absolute;
  right: 2rem;
  top: 7rem;
  margin-top: 0;
  height: calc(100vh - 8rem);
  width: 22rem;
  background-color: #00ff00;
  overflow: scroll;
  overflow-x: hidden;
}
.botton {
  display: block;
  margin: auto;
  border-radius: 50%;
  color: #00ff00;
  border: 2px solid white;
  margin-top: 1rem;
  background-color: white;
  font-size: 40px;
  width: 2rem;
  height: 2rem;
  line-height: 0;
  padding: 0;
}
.botton:hover {
  background-color: orange;
}
.topname {
  color: white;
  text-align: center;
  padding-top: 22px;
  font-weight: thin;
  font-size: 24px;
  line-height: 36px;
  -webkit-text-decoration-color: white; /* Safari */
  text-decoration-color: white;
  position: relative;
}
.topname:after {
  content: "";
  width: 33%;
  position: absolute;
  left: 7.4rem;
  top: 3.5rem;
  border-width: 0 0 1px;
  border-style: solid;
}
/deep/ .form-control {
  border-radius: 3rem !important;
}
/* width */
::-webkit-scrollbar {
  width: 5px;
  border-right: 2rem solid transparent;
}

/* Track */
::-webkit-scrollbar-track {
  background: white;
  /* background: var(--bg-color); */
}

/* Handle */
::-webkit-scrollbar-thumb {
  /* background: #888; */
  background: orange;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  /* background: #555; */
  background: red;
}
</style>