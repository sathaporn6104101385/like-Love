<template>
  <div>
    <div>
      <button class="btn  " @click="upFunction5">
        <b class="fs"
          >👍 <br />
          <p class="fs2">+5</p></b
        >
      </button>
      <button class="btn  " @click="upFunction10">
        <b class="fs"
          >😍 <br />
          <p class="fs2">+10</p></b
        >
      </button>
      <button class="btn  " @click="upFunction15">
        <b class="fs"
          >😆 <br />
          <p class="fs2">+15</p></b
        >
      </button>
      <button class="btn  " @click="downFunction10">
        <b class="fs"
          >😂 <br />
          <p class="fs2">-10</p></b
        >
      </button>
      <button class="btn  " @click="downFunction20">
        <b class="fs"
          >😡 <br />
          <p class="fs2">-20</p></b
        >
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      counter: 0,
    };
  },

  methods: {
    upFunction5: function() {
      this.counter += 5;
      this.$emit("cc", this.counter);
    },
    upFunction10: function() {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },
    upFunction15: function() {
      this.counter += 15;
      this.$emit("cc", this.counter);
    },
    downFunction10: function() {
      this.counter -= 10;
      this.$emit("cc", this.counter);
    },
    downFunction20: function() {
      this.counter -= 20;
      this.$emit("cc", this.counter);
    },
  },
};
</script>

<style>
.fs {
  font-size: 40px;
  color: aqua;
}
.fs2 {
  font-size: 20px;
}
</style>
