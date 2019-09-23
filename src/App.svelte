<script>
  import Box from "./Box.svelte";
  import AddBtn from "./AddBtn.svelte";
  import Getcode from "./Getcode.svelte";

  function handleClick() {
    alert("添加微信：Clovelee0216");
  }
</script>

<style>
  :global(body) {
    background-color: #fff;
    margin: 0;
    color: #232323;
  }
  p {
    line-height: 28px;
  }
  .header {
    line-height: 5em;
    display: flex;
    justify-content: space-between;
    position: fixed;
    width: 100%;
    background-color: #7d10f2;
    z-index: 10;
    color: #fff;
  }
  .logo {
    padding-left: 2em;
  }
  .logo img {
    width: 52px;
    height: 52px;
    vertical-align: middle;
  }
  .logo span {
    font-weight: bold;
    font-size: 1em;
    vertical-align: middle;
  }
  .nav {
    color: #000;
    padding-right: 2em;
  }
  .nav a {
    padding: 4px 0.5em;
    font-size: 12px;
    color: #232323;
    background-color: pink;
    border-radius: 4px;
  }
  h1 {
    color: #232323;
  }

  .p1,
  .p2,
  .p3,
  .p4,
  .p5,
  .p6,
  .p7 {
    padding: 4em;
  }
  .p1 span,
  .p2 span,
  .p3 span,
  .p4 span,
  .p5 span,
  .p6 span,
  .p7 span {
    display: inline-block;
    font-style: oblique;
    font-weight: 500;
    margin-right: 0.5em;
    padding: 0.2em;
    text-decoration: wavy underline;
  }
  .p1 span {
    text-decoration-color: aquamarine;
  }
  .p2 span {
    text-decoration-color: brown;
  }
  .p3 span {
    text-decoration-color: plum;
  }
  .p4 span {
    text-decoration-color: darkgoldenrod;
  }
  .p5 span {
    text-decoration-color: pink;
  }
  .p6 span {
    text-decoration-color: darkcyan;
  }
  .p7 span {
    text-decoration-color: rgb(255, 200, 200);
  }

  .home {
    background-color: #7d10f2;
    padding: 6em 3em 4em 3em;
    color: #fff;
  }
  .home h1 {
    color: #fff;
  }
  .home p {
    margin-bottom: 2em;
  }
  .home b {
    color: yellow;
    font-style: italic;
    text-decoration: wavy underline;
  }
  .p1 img,
  .p3 img,
  .p5 img,
  .p7 img {
    float: right;
    width: 40px;
  }
  .p2 img,
  .p4 img,
  .p6 img {
    float: left;
    width: 40px;
  }
  .p1 h2 {
    background-color: aquamarine;
  }
  .p1 p {
    background-color: #fff;
  }
  .p2 {
    background-color: mistyrose;
  }
  .p2 h2,
  .p4 h2,
  .p6 h2 {
    background-color: #fff;
  }
  .p3 h2 {
    background-color: plum;
  }
  .p4 {
    background-color: rgb(255, 229, 200);
  }
  .p5 h2 {
    background-color: pink;
  }
  .p6 {
    background-color: powderblue;
  }
  .p7 h2 {
    background-color: rgb(255, 200, 200);
  }
  .footer {
    padding: 4em;
    background-color: whitesmoke;
  }
  .footer b {
    margin-bottom: 0.5em;
    display: block;
  }
  .footer img {
    padding: 2em;
  }
  .contact {
    margin: 0 auto;
    display: block;
  }
</style>

<!--
	API：https://api.sheety.co/c30cf8e9-2755-41e6-9875-e7aa3625d4fa

	const ASSETS = `https://svelte-assets.surge.sh/crossfade`;
 -->
<svelte:head>
  <title>花糖-正品美妆代理</title>
</svelte:head>

<div class="header">
  <div class="logo">
    <img src="favicon.png" alt="" />
    <span>花糖</span>
  </div>
  <div class="nav">
    <a href="black">美代直入···</a>
  </div>
</div>

<div class="home">
  <h1>零成本开启你的轻创业之旅</h1>
  <p>
    花糖致力于打造全新个人美业代理的供应服务一体平台；成为花糖美代的一员，可低价享受全球正品品牌优质产品，并且每月额外增收可达到
    <b>3000元</b>
    ，更有万元高收入等你来开创～～～
  </p>
  <Getcode />
</div>

<div class="p1">
  <img src="pattern1.png" alt="" />
  <h2>进口品牌美妆 好物由你所选</h2>
  <p>
    花糖谨选顶级供应商，提供数千sku国际品牌护肤美妆用品，确保品牌产品来源，让更多人能够享受到正品优质产品。
  </p>
  <span>超多大牌</span>
  <span>热门爆款</span>
  <span>限价代理</span>
</div>

<div class="p2">
  <img src="pattern2.png" alt="" />
  <h2>一键最低价 与百万卖家同价</h2>
  <p>
    无传统分级层层代理的价格套系，直接对接顶级供应商的提供最低产品代理价，具体售卖价格由美代自主设定，更多价格空间，助力完成更多交易。
  </p>
  <span>统一代理</span>
  <span>一键最低</span>
  <span>自主定价</span>

</div>

<div class="p3">
  <img src="pattern5.png" alt="" />
  <h2>美好之物 均值得分享及赞扬</h2>
  <p>
    选择花糖内的产品，一键分享至微博、微信好友、朋友圈或线下等私有社交圈，提供护肤美妆建议及服务，获得大家的认可，赚取适当的利益。
  </p>
  <span>一键转发</span>
  <span>尽情开拓</span>
  <span>多维收获</span>
</div>

<div class="p4">
  <img src="pattern4.png" alt="" />
  <h2>无压货风险 无时间空间限制</h2>
  <p>
    不必花费大量资金成本，购买及存储商品，完全零成本零库存；不必局限于小小柜台，在任意时间地点，只需简单分享好物，都可以轻轻松松完成的交易。
  </p>
  <span>零库存</span>
  <span>零成本</span>
  <span>随时开展业务</span>
</div>

<div class="p5">
  <img src="pattern6.png" alt="" />
  <h2>优质供应 全站保证品牌正品</h2>
  <p>
    不影响二次出售产品，接受无理由退货，退货运费由买家承担；已开包装影响二次出售，可折价回收；已使用产品，不接受退换货。
  </p>
  <span>正品保证</span>
  <span>退货无忧</span>
</div>

<div class="p6">
  <img src="pattern3.png" alt="" />
  <h2>即时单笔结算 一件代发全国</h2>
  <p>
    单笔订单无论金额大小，先结算后发货；代理价格不含运费，全国运费一件6元起，超重补差价，以实际运费为准。
  </p>
  <span>一件代发</span>
  <span>实时结算</span>
</div>

<div class="p7">
  <img src="pattern7.png" alt="" />
  <h2>限时免费申请 还有更多奖励</h2>
  <p>
    限时免费申请代理，完全零成本；享受最低代理价格，还能拿到高额返利；邀请好友做代理，同样获得购物津贴，更多奖励等你来拿～
  </p>
  <span>免费申请</span>
  <span>奖励多多</span>
</div>

<div class="footer">
  <h2>花糖美代 期待你的加入</h2>
  <p>1000多款热门进口品牌，供你选择，省更多赚更多～～～</p>
  <b>扫码二维码加关注 快速获取免费代理资格</b>
  <img class="contact" src="WX03.png" alt="" />
</div>
