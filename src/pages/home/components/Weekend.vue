<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '001',
        imgUrl: '//h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/973dc1ae0da73a58410186df08ff25cb.jpg',
        title: '杭州-俄罗斯',
        desc: '杭州直飞❀用券立减200，俄罗斯/莫斯科/圣彼得堡+金环谢镇深度8日！免签'
      }, {
        id: '002',
        imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/488809ef-1ba1-4cb4-be70-98fd20e21919.jpg_r_480x320x90_2b3d7b48.jpg',
        title: '杭州',
        desc: '酒店'
      }, {
        id: '003',
        imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/87aeafc1-a3e9-49dd-b261-f2cc21a42cfa.jpg_r_480x320x90_6de706bb.jpg',
        title: '俄罗斯',
        desc: '机票'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 32%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
