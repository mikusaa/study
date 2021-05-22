<template>
<div id="post-card">

<span v-if="count">{{ fomartDate(date) }} + {{ count }} 字</span>
<div id="title"><b>制作原神个人信息名片</b></div>
  <div id="subtitle">
      使用「原神玩家信息卡片生成工具」，生成你的个人原神名片。
    </div>
</div>
</template>

<script>
export default {
  name: "PostCard",
  props: {
    count: {
      type: Number,
      default: 0,
    },
    date: {
      type: String,
      default: "20210101",
    },
  },
  data() {
    return {};
  },
  methods: {
    fomartDate(date) {
      let year, month, day;
      year = date.substring(0, 4);
      month = date.substring(4, 6);
      day = date.substring(6, 8);
      let newDate = `${month} ${day}, ${year}`;
      return newDate;
    },
  },
};
</script>


<style scoped>
#post-card {
  background-image: url(https://i.mikusa.cn/img-original/img/2021/01/05/02/26/58/86829113_p0.jpg);
  background-size: cover;
  width: 600px;
  height: 150px;
  margin: 16px;
  float: left;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
  padding: 16px;
}
#title {
  font-size: 24px;
  padding: 16px 0;
}
#subtitle {
  font-size: 18px;
  text-align: left;
}
</style>
