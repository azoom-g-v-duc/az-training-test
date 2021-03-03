<template>
  <div class="related-news">
    <div class="left">
      <div class="news">
        <h2 class="title">Thông tin mới</h2>
        <div class="item" v-for="(thread, index) in threads" :key="index">
          <div class="container">
            <img class="thumbnail" :src="thread.thumbnail" />
            <div class="wraper">
              <h3 class="title">{{ thread.title }}</h3>
              <p class="content">{{ thread.content }}</p>
              <div class="info">
                <img class="avatar" :src="thread.info.avatar" />
                <span class="author"> {{ thread.info.author }} </span>
                <span class="since">
                  <span>&nbsp;-&nbsp;</span><span>{{ thread.info.since }}</span>
                </span>
                <span class="forum">
                  <span>&nbsp;-&nbsp;</span><span>{{ thread.info.forum }}</span>
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right">
      <div class="title">Những anh em tích cực nhất</div>
      <div class="members">
        <div class="member">
          <img class="avatar" />
          <div class="information">
            <div class="header">
              <div class="points"></div>
              <div class="rank"></div>
            </div>
            <div class="name"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    threads() {
      return [
        {
          thumbnail:
            'https://imgproxy3.cdnforo.com/XTMh-hD_ycmRKPOui9rVmWZtDp2d_Q1AUzs069EItAE/h:460/plain/http://data.tinhte.vn/data/attachment-files/2021/03/5373819_IMG_0740.jpg',
          title: 'Review ngắn máy pha cà phê La marzocco linea mini 130 triệu',
          content:
            'Đây là review về Review ngắn máy pha cà phê của mình. Mình mua nó với giá 130 triệu. Hi vọng phần review sẽ hữu ích cho bạn nào muốn mua nhé, nếu bạn có câu hỏi gì thì hãy comment vô bài này nha.',
          info: {
            avatar:
              'https://tinhte.vn/styles/uiflex/xenforo/avatars/avatar_m.png',
            author: 'magic.flame',
            since: '1h',
            forum: 'Điện tử - Tiêu dùng'
          }
        }
      ]
    },
    members() {
      return []
    }
  }
}
</script>

<style>
.related-news {
  font-size: 16px;
  padding: 0 20px;
  max-width: 1144px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
}

.related-news > .right > .title {
  display: block;
  font-family: Roboto, sans-serif;
  font-weight: 700;
  font-size: 18px;
  line-height: 21px;
  text-decoration: none;
  cursor: pointer;
}
.related-news > .left {
  min-width: 576;
  display: flex;
  flex-wrap: wrap;
  flex: 1 1 0;
}
.related-news > .news {
  margin-bottom: 25px;
  display: list-item;
  text-align: -webkit-match-parent;
}
.related-news > .left > .news > .title {
  text-align: left;
  font-size: 18px;
  font-weight: 900;
  margin-bottom: 16px;
}
.related-news > .left > .news > .item {
  display: block;
  margin-bottom: 30px;
  position: relative;
}

.related-news > .left > .news > .item > .container > .thumbnail {
  width: 240px;
  height: 148px;
  top: 0;
  left: 0;
}
.related-news > .left > .news > .item > .container {
  display: flex;
}
.related-news > .left > .news > .item > .container > .wraper > .title {
  font-size: 18px;
  font-weight: 900;
}
.related-news > .left > .news > .item > .container > .wraper > .content {
  margin-top: 11px;
  color: #222b45;
  display: block;
}
.related-news > .left > .news > .item > .container > .wraper > .info {
  color: #8f9bb3;
  font-size: 12px;
  margin-top: 12px;
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  -webkit-box-pack: justify;
}
.related-news > .left > .news > .item > .container > .wraper > .info > .avatar {
  max-width: 100%;
  margin-right: 5px;
  width: 28px;
  height: 28px;
  float: left;
  border-radius: 100%;
  background-color: #e5e6ec;
}
.related-news > .left > .news > .item > .container > .wraper > .info > .author {
  font-weight: 700;
  color: #0768ea;
}
</style>
