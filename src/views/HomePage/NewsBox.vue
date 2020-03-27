<template>
    <div id="newsbox">
      <el-row :gutter="10">
        <el-col :span="12">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>新闻资讯</span>
              <el-button style="float: right; padding: 3px 0" type="text" @click="searchMore">更多>></el-button>
            </div>
            <div>
            <ul>
              <li v-for="(news1, index) in newsDetails1" :key="index" v-if="index<3">
                <a :href="news1.url" class="fly-avatar">
                  <img :src="news1.imgUrl" style="width: 45px; height: 45px;">
                </a>
                <el-row type="flex" justify="space-between">
                  <el-col :span="18">
                    <div class="overflow">
                      <a :href="news1.url" class="news-title">{{news1.title}}</a>
                    </div>
                  </el-col>
                  <el-col :span="2">
                    <el-tag effect="dark" color="#FF5722" size="small" style="border: none;">news</el-tag>
                  </el-col>
                </el-row>

                <el-row type="flex" justify="space-between">
                  <el-col :span="15">
                    <el-tag effect="dark" color="#1E9FFF" size="small" style="border: none;">{{news1.time | formatDate}}</el-tag>
                    <el-tag effect="dark" color="#FFB800" size="small" style="border: none;">{{news1.author}}</el-tag>
                    <el-tag effect="dark" color="#009688" size="small" style="border: none;">{{news1.department}}</el-tag>
                  </el-col>
                  <el-col :span="2.5">
                    <span class="comment">评论:{{news1.comment}}</span>
                  </el-col>
                </el-row>
              </li>
            </ul>
          </div>
          </el-card>
        </el-col>

        <el-col :span="12">
          <el-card  class="box-card">
            <div slot="header" class="clearfix">
              <span>政策文件</span>
              <el-button style="float: right; padding: 3px 0" type="text">更多>></el-button>
            </div>
            <div>
              <ul>
                <li v-for="(news2, index) in newsDetails2" :key="index" v-if="index<3">
                  <a :href="news2.url" class="fly-avatar">
                    <img :src="news2.imgUrl" style="width: 45px; height: 45px;">
                  </a>
                  <el-row type="flex" justify="space-between">
                    <el-col :span="18">
                      <div class="overflow">
                        <a :href="news2.url" class="news-title">{{news2.title}}</a>
                      </div>
                    </el-col>
                    <el-col :span="2">
                      <el-tag effect="dark" color="#FF5722" size="small" style="border: none;">news</el-tag>
                    </el-col>
                  </el-row>

                  <el-row type="flex" justify="space-between">
                    <el-col :span="15">
                      <el-tag effect="dark" color="#1E9FFF" size="small" style="border: none;">{{news2.time | formatDate}}</el-tag>
                      <el-tag effect="dark" color="#FFB800" size="small" style="border: none;">{{news2.author}}</el-tag>
                      <el-tag effect="dark" color="#009688" size="small" style="border: none;">{{news2.department}}</el-tag>
                    </el-col>
                    <el-col :span="2.5">
                      <span class="comment">评论:{{news2.comment}}</span>
                    </el-col>
                  </el-row>
                </li>
              </ul>
            </div>
          </el-card>
        </el-col>
      </el-row>

      <el-row :gutter="10">
        <el-col :span="12">
          <el-card  class="box-card">
            <div slot="header" class="clearfix">
              <span>工作动态</span>
              <el-button style="float: right; padding: 3px 0" type="text">更多>></el-button>
            </div>
            <div>
              <ul>
                <li v-for="(news3, index) in newsDetails3" :key="index" v-if="index<3">
                  <a :href="news3.url" class="fly-avatar">
                    <img :src="news3.imgUrl" style="width: 45px; height: 45px;">
                  </a>
                  <el-row type="flex" justify="space-between">
                    <el-col :span="18">
                      <div class="overflow">
                        <a :href="news3.url" class="news-title">{{news3.title}}</a>
                      </div>
                    </el-col>
                    <el-col :span="2">
                      <el-tag effect="dark" color="#FF5722" size="small" style="border: none;">news</el-tag>
                    </el-col>
                  </el-row>

                  <el-row type="flex" justify="space-between">
                    <el-col :span="15">
                      <el-tag effect="dark" color="#1E9FFF" size="small" style="border: none;">{{news3.time | formatDate}}</el-tag>
                      <el-tag effect="dark" color="#FFB800" size="small" style="border: none;">{{news3.author}}</el-tag>
                      <el-tag effect="dark" color="#009688" size="small" style="border: none;">{{news3.department}}</el-tag>
                    </el-col>
                    <el-col :span="2.5">
                      <span class="comment">评论:{{news3.comment}}</span>
                    </el-col>
                  </el-row>
                </li>
              </ul>
            </div>
          </el-card>
        </el-col>

        <el-col :span="12">
          <el-card  class="box-card">
            <div slot="header" class="clearfix">
              <span>党建事务</span>
              <el-button style="float: right; padding: 3px 0" type="text">更多>></el-button>
            </div>
            <div>
              <ul>
                <li v-for="(news4, index) in newsDetails4" :key="index" v-if="index<3">
                  <a :href="news4.url" class="fly-avatar">
                    <img :src="news4.imgUrl" style="width: 45px; height: 45px;">
                  </a>
                  <el-row type="flex" justify="space-between">
                    <el-col :span="18">
                      <div class="overflow">
                        <a :href="news4.url" class="news-title">{{news4.title}}</a>
                      </div>
                    </el-col>
                    <el-col :span="2">
                      <el-tag effect="dark" color="#FF5722" size="small" style="border: none;">news</el-tag>
                    </el-col>
                  </el-row>

                  <el-row type="flex" justify="space-between">
                    <el-col :span="15">
                      <el-tag effect="dark" color="#1E9FFF" size="small" style="border: none;">{{news4.time | formatDate}}</el-tag>
                      <el-tag effect="dark" color="#FFB800" size="small" style="border: none;">{{news4.author}}</el-tag>
                      <el-tag effect="dark" color="#009688" size="small" style="border: none;">{{news4.department}}</el-tag>
                    </el-col>
                    <el-col :span="2.5">
                      <span class="comment">评论:{{news4.comment}}</span>
                    </el-col>
                  </el-row>
                </li>
              </ul>
            </div>
          </el-card>
          <el-card  class="box-card">
            <div slot="header" class="clearfix">
              <span>在线学习</span>
              <el-button style="float: right; padding: 3px 0" type="text">更多>></el-button>
            </div>
            <div>
              <ul>
                <li v-for="(news5, index) in newsDetails5" :key="index" v-if="index<3">
                  <a :href="news5.url" class="fly-avatar">
                    <img :src="news5.imgUrl" style="width: 45px; height: 45px;">
                  </a>
                  <el-row type="flex" justify="space-between">
                    <el-col :span="18">
                      <div class="overflow">
                        <a :href="news5.url" class="news-title">{{news5.title}}</a>
                      </div>
                    </el-col>
                    <el-col :span="2">
                      <el-tag effect="dark" color="#FF5722" size="small" style="border: none;">news</el-tag>
                    </el-col>
                  </el-row>

                  <el-row type="flex" justify="space-between">
                    <el-col :span="15">
                      <el-tag effect="dark" color="#1E9FFF" size="small" style="border: none;">{{news5.time | formatDate}}</el-tag>
                      <el-tag effect="dark" color="#FFB800" size="small" style="border: none;">{{news5.author}}</el-tag>
                      <el-tag effect="dark" color="#009688" size="small" style="border: none;">{{news5.department}}</el-tag>
                    </el-col>
                    <el-col :span="2.5">
                      <span class="comment">评论:{{news5.comment}}</span>
                    </el-col>
                  </el-row>
                </li>
              </ul>
            </div>
          </el-card>
        </el-col>
      </el-row>

    </div>
</template>

<script>
  const
    s = 1000,
    m = 60 * s,
    h = 60 * m,
    d = 24 * h,
    mo = 30 * d,
    y = 365 * d;

  const fdate = [
    {
      time: y,
      text: '年'
    },
    {
      time: mo,
      text: '月'
    },
    {
      time: d,
      text: '天'
    },
    {
      time: h,
      text: '小时'
    },
    {
      time: m,
      text: "分钟"
    },
    {
      time: s,
      text: '秒'
    }
  ];

    export default {
      data() {
        return {
          newsDetails1: [
            {
              id: 192,
              title: '脱贫摘帽不是终点，而是新起点 ——习近平总书记在决战决胜脱贫攻坚座谈会上重要讲话引发强烈反响',
              imgUrl: require('../../assets/newsPic/192.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?message&192',
              time: '2020-3-11 6:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 191,
              title: '李克强对森林草原防灭火工作作出重要批示',
              imgUrl: require('../../assets/newsPic/191.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?message&191',
              time: '2020-3-11 6:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 190,
              title: '习近平：毫不放松抓紧抓实抓细各项防控工作 坚决打赢湖北保卫战武汉保卫战',
              imgUrl: require('../../assets/newsPic/190.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?message&190',
              time: '2020-3-11 6:00:00',
              author: '朱雪梅',
              department: '河北省',
              comment: 0
            }
          ],
          newsDetails2: [
            {
              id: 95,
              title: '中办国办印发通知 组织29个工作组开展复工复产情况调研',
              imgUrl: require('../../assets/newsPic/95.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?policy&95',
              time: '2020-3-13 00:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 94,
              title: '五项措施保障困难群众基本生活（国务院联防联控机制发布会）',
              imgUrl: require('../../assets/newsPic/93.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?policy&94',
              time: '2020-3-10 00:00:00',
              author: '朱雪梅',
              department: '河北省',
              comment: 0
            },
            {
              id: 93,
              title: '（受权发布）中共中央 国务院关于深化医疗保障制度改革的意见',
              imgUrl: require('../../assets/newsPic/93.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?policy&93',
              time: '2020-3-6 00:00:00',
              author: '朱雪梅',
              department: '河北省',
              comment: 0
            }
          ],
          newsDetails3: [
            {
              id: 224,
              title: '李克强主持召开中央应对新冠肺炎疫情工作领导小组会议 要求根据疫情形势变化分区分级做好防控和保障工作',
              imgUrl: require('../../assets/newsPic/224.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?work&224',
              time: '2020-3-13 00:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 223,
              title: '习近平总书记重要讲话让武汉市东湖新城社区干部群众备受鼓舞，他们一致表示—— 越到关键时候 越是不能松劲',
              imgUrl: require('../../assets/newsPic/223.jpeg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?work&223',
              time: '2020-3-11 6:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 222,
              title: '中央指导组：同湖北人民和武汉人民并肩战斗 坚决打赢湖北保卫战、武汉保卫战',
              imgUrl: require('../../assets/newsPic/222.jpeg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?message&222',
              time: '2020-3-12 00:00:00',
              author: '朱雪梅',
              department: '河北省组织部',
              comment: 0
            }
          ],
          newsDetails4: [
            {
              id: 25,
              title: '测试数据',
              imgUrl: require('../../assets/newsPic/default.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?activity&25',
              time: '2019-11-5 00:00:00',
              author: '张芸磊',
              department: '河北省',
              comment: 0
            }
          ],
          newsDetails5: [
            {
              id: 2257,
              title: '战疫情保春耕 不误农时不负春',
              imgUrl: require('../../assets/newsPic/2257.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?study&2257',
              time: '2020-3-13 14:00:00',
              author: '张芸磊',
              department: '河北省组织部',
              comment: 0
            },
            {
              id: 2197,
              title: '河北支援湖北医疗队24名队员在抗疫一线入党',
              imgUrl: require('../../assets/newsPic/2197.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?study&2197',
              time: '2020-3-9 00:00:00',
              author: '张芸磊',
              department: '河北省',
              comment: 0
            },
            {
              id: 2069,
              title: '组织全动员 党员挺在前 河北省各级党组织和广大党员坚守岗位履职担当 在疫情防控一线践行初心使命',
              imgUrl: require('../../assets/newsPic/2069.jpg'),
              url: 'https://www.taiyouinfo.cn/dangJian/article.html?study&2069',
              time: '2020-2-20 00:00:00',
              author: '张芸磊',
              department: '河北省',
              comment: 0
            }
          ]
        }
      },
      methods: {
        searchMore() {
          window.location.href = "http://www.baidu.com/"
        }
      },
      filters: {
        formatDate(value) {
          // s m h d mo y
          // 计算出时间差
          const time = Date.now() - new Date(value);
          for (let i = 0; i < fdate.length; i++) {
            const t = time / fdate[i].time;
            if (t >= 1) {
              return Math.floor(t) + fdate[i].text + '前'
            }
          }
        }
      }
    }
</script>

<style scoped>
  #newsbox {
    margin-top: 20px;
    line-height: normal;
  }

  #newsbox li {
    height: auto;
  }

  .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .box-card {
    width: 100%;
    margin-bottom: 5px;
    margin-top: 5px;
  }

  .box-card ul {
    display: block;
    list-style-type: disc;
    margin: 0;
    padding: 0;
  }

  .box-card li {
    list-style: none;
    position: relative;
    height: 45px;
    line-height: 22px;
    padding: 15px 15px 15px 75px;
    border-bottom: 1px dotted #e2e2e2;
  }

  .fly-avatar {
    color: #333;
    text-decoration: none;
    position: absolute;
    left: 15px;
    top: 15px;
  }

  .news-title {
    text-decoration: none;
    color: #333333;
  }

  .news-title:hover {
    color: #009688;
  }

  .overflow {
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
  }

  .comment {
    color: #999999;
    font-size: 12px;
  }
</style>
