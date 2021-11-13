<template>
  <div class="demo" :style="contentStyle">
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>This is a demo!</p>
    <p>这是一段测试代码，今天是2021年11月11日</p>
  </div>
</template>
<script>
import config from "../plugins/config";
export default {
  name: "pcontent",
  data() {
    return {
      contentStyle: {
        fontFamily: config.fonts[this.$store.state.config.font],
        fontSize: this.$store.state.config.fontSize + "px"
      }
    };
  },
  // props: ["carray"],
  // render() {
  //   const { fontFamily, fontSize } = this;
  //   let style = fontFamily;
  //   style.fontSize = fontSize;
  //   if (this.show) {
  //     return (
  //       <div>
  //         {this.carray.map(a => {
  //           return <p style={style} domPropsInnerHTML={a} />;
  //         })}
  //       </div>
  //     );
  //   } else {
  //     return <div />;
  //   }
  // },
  computed: {
    // show() {
    //   return this.$store.state.showContent;
    // },
    fontFamily() {
      return config.fonts[this.$store.state.config.font];
    },
    fontSize() {
      return this.$store.state.config.fontSize + "px";
    }
  },
  watch: {
    // 当字体的样式发生变化时就进行回调
    fontSize() {
      // let that = this;
      // that.$store.commit("setShowContent", false);
      // this.$nextTick(() => {
      //   that.$store.commit("setShowContent", true);
      // });
      this.contentStyle.fontSize = this.$store.state.config.fontSize + "px";
    },
    fontFamily() {
      // 注意返回的是对象！
      this.contentStyle.fontFamily =
        config.fonts[this.$store.state.config.font].fontFamily;
    }
  }
};
</script>

<style lang="stylus" scoped>
p {
  display: block;
  word-wrap: break-word;
  word-break: break-all;
}
</style>
