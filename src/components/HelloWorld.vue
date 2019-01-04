<template>
  <div class="hello">    
    <h1>Are you like this?</h1>    
    
    <div class="org_likeArea" v-on:click="toggle" v-show="tgl">
      <h2 v-show="showMsg">{{ msg }}</h2>
      <h2 v-show="showText">{{ tex }}</h2>

      <transition>
      <div class="org_mark" v-bind:class='{active:isActive}' v-if="this.showText">
        <p class="m_like"><span class="a_mark add">♡</span></p>
        <p class="a_count">{{ count + 1 }}</p>
      </div>
      <div class="org_mark" v-else>
        <p class="m_like"><span class="a_mark">♡</span></p>
        <p class="a_count">{{ count }}</p>
      </div>
      </transition>  
    </div>        
  
  </div>
</template>

<script>
export default {
  data() {
    return {
      tgl: 'toggle',
      msg: 'Please like!',
      tex: 'Remove like...',
      isActive: true,
      showMsg: true,
      showText: false,
      count: 1,
    };
  },
  methods: {
    toggle: function() {
      this.showText = !this.showText;
      this.showMsg = !this.showMsg;
      //       this.count = this.count;
      //       count = count + 1;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss' scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

button.btn {
  padding: 15px 20px;
}
.active .add {
  color: red;
}

.org_likeArea {
  //   background: #eee;
  cursor: pointer;
  width: fit-content;
  margin: auto;
}

.org_mark {
  //   background: aliceblue;
  //   display: flex;
  display: inline-flex;
  align-items: center;
}
.m_like {
  //   transition: 0.3s;
  position: relative;
  .a_mark {
    font-size: 20px;
    &.add {
      animation-name: sizeScale;
      animation-duration: 0.3s;
    }
  }
  .a_count {
    position: absolute;
    right: 0;
    top: 50%;
  }
}
@keyframes sizeScale {
  0% {
    font-size: 20px;
  }
  20% {
    font-size: 28px;
  }

  50% {
    font-size: 24px;
  }

  100% {
    font-size: 20px;
  }
}
</style>
