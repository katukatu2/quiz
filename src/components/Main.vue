<template>
  <div class="main">
    <div>{{title}}</div>
    <h2>{{question}}</h2>
    <span
      @click="superClick(index,correct);"
      class="ansers"
      v-for="(anser, index) in ansers"
      v-bind:key="anser"
    >{{anser}}</span>
  </div>
</template>

<script>
import quiz from "../assets/quiz.json"; //クイズjsonファイルの読み出し
console.log(quiz);
export default {
  data() {
    return {
      title: "中国語日常会話1",
      question: quiz[0].question,
      ansers: quiz[0].ansers,
      correct: quiz[0].correct
    };
  },
  methods: {
    superClick(value, correct) {
      //正解であればアラート
      console.log(correct);
      if (value == correct) {
        alert("正解！");
      }
    }
  }
};
</script>

<style scoped>
.main {
  font-size: 20px;
  padding: 20px;
}
.ansers {
  padding: 0 10px 0 0;
}
.body {
  margin: 0;
}
</style>