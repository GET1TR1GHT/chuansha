<template>
  <div>
    <img src="./images/image-city.png" class="image-city"/>
    <div id="container">
      <div class="xiaoyang">
        <img >
        <p>{{chuansha.store_brand}}</p>
      </div>

      <div class="container-header">
        <div class="title">
          <p class="charset">营业执照</p>
          <div class="shape-together">
            <img src="./images/icon-division.png" class="circle"/>
            <div class="line"></div>
          </div>
        </div>
        <div class="user">
          <div class="user-icon">
            <img src="./images/image-head.png" class="icon"/>
          </div>
          <div class="user-message">
            <div class="row row1">
              <p>{{ chuansha.store_license_operator }}</p>
              <p>{{ chuansha.store_name }}</p>
            </div>
            <div class="row row2">
              <p>成立日期：{{ chuansha.store_license_date }}</p>
            </div>
            <div class="row row3">
              <p>经营范围：{{chuansha.store_license_scope}}</p>
            </div>
          </div>
        </div>
      </div>

      <div class="col">
        <ul>
          <li>
            <p class="pp">名称</p>
            <span class="bb">{{chuansha.store_license_name}}</span>
          </li>
          <li>
            <p class="pp">统一社会信用码</p>
            <span class="bb">{{chuansha.store_license_code}}</span>
          </li>
          <li>
            <p class="pp">营业场所</p>
            <span class="bb">{{chuansha.store_license_address}}</span>
          </li>
        </ul>
      </div>

      <div class="col1">
        <div class="title">
          <p class="charset">食品经营及相关许可/备案</p>
          <div class="shape-together">
            <img src="./images/icon-division.png" class="circle"/>
            <div class="line"></div>
          </div>
        </div>
        <div class="Permit" v-for="filing in chuansha.store_filings">
            <p>许可证编号：{{ filing.store_filing_code ? filing.store_filing_code : '暂无' }}</p>
            <h2>经营项目：{{ filing.store_filing_project}}</h2>
            <span>有效期至：{{ filing.store_filing_date}}</span>
        </div>
      </div>

      <div class="col2">
        <div class="menu menu1">
          <div class="title">
            <p class="charset">脸谱评级</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <ul class="star">
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-unfilled.png"/></li>
            <li><img src="./images/icon-star-unfilled.png"/></li>
          </ul>
        </div>
        <div class="menu menu2">
          <div class="title">
            <p class="charset">消费投诉电话</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{chuansha.store_consume_complain_number}}</p>
        </div>
        <div class="menu menu3">
          <div class="title">
            <p class="charset">店内负责人姓名</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{chuansha.store_responsible_person}}</p>
        </div>
        <div class="menu menu4">
          <div class="title">
            <p class="charset">商场管理评级</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <ul class="star">
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-filled.png"/></li>
            <li><img src="./images/icon-star-unfilled.png"/></li>
            <li><img src="./images/icon-star-unfilled.png"/></li>
          </ul>
        </div>
        <div class="menu menu5">
          <div class="title">
            <p class="charset">行政处罚记录</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{ chuansha.store_admin_punish_records }}</p>
        </div>
        <div class="menu menu6">
          <div class="title">
            <p class="charset">重大消费纠纷记录</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{ chuansha.store_consume_dispute_records }}</p>
        </div>
        <div class="menu menu7">
          <div class="title">
            <p class="charset">产品保修</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{
            chuansha.store_product_care ? chuansha.store_product_care : '暂无'
            }}</p>
        </div>
        <div class="menu menu8">
          <div class="title">
            <p class="charset">产品使用说明、食品保质期</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{
            chuansha.store_product_instructions  ?chuansha.store_product_instructions : '暂无'
            }}</p>
        </div>
        <div class="menu menu9">
          <div class="title">
            <p class="charset">外卖电话</p>
            <div class="shape-together">
              <img src="./images/icon-division.png" class="circle"/>
              <div class="line"></div>
            </div>
          </div>
          <p class="xi">{{
            chuansha.store_take_out_numbers ? chuansha.store_take_out_numbers : '暂无'
            }}</p>
        </div>
      </div>

      <div class="footer">
        <p>扫码分享</p>
        <div class="hehe"></div>
        <div class="code"><img :src="chuansha.store_qrcode"></div>
      </div>
    </div>
  </div>
</template>

<script type="text/javascript">
  import Data from './base/data.js';

  export default {
    data () {
      let query = window.location.search.slice(1);
      query = query.split('=');
      let id = query[1];
      let _data;

      for(let i in  Data){
        if(Data[i].id == id){
          _data = Data[i];
          break;
        }
      }

      console.log(_data)

      if (_data) {
        return {
          chuansha: _data
        }
      } else return {
        chuansha: Data[0]
      }
    },
    create(){
      console.log(this.chuansha)
    },
    methods: {
      Data (id) {

      }
    }
  }
</script>

<style>
  body {
    background: url("./images/image-map.png") no-repeat top center;
    background-size: 100%;
    padding: 0 6%;
  }

  .image-city {
    width: 270px;
    height: 158px;
    clear: both;
    display: block;
    margin: 0 auto;
    margin-top: 57px;
  }

  #container {
    width: 92%;
    min-height: 650px;
    background: rgba(255, 255, 255, 1);
    box-shadow: 0 1px 5px rgba(0, 0, 0, 0.35);
    margin-bottom: 65px;
    border: 0;
    padding: 0 4%;
  }

  .xiaoyang {
    width: 101px;
    height: 118px;
    clear: both;
    display: block;
    margin: 0 auto;
    background: url("./images/icon-flag.png") no-repeat center center;
    background-size: 100% 100%;
    text-align: center;
    padding: 10px 0;
  }
  .xiaoyang img{
    width: 50px;
    height: 50px;
    border: 1px solid #ccc;
    border-radius: 50px;
  }
  .xiaoyang p{
    color: rgba(255,203,152,1);
  }
  .container-header {
    margin-top: 25px;
    min-height: 200px;
    overflow: hidden;
    margin-bottom: 15px;
  }

  .title {
    width: 100%;
    height: 20px;
    line-height: 20px;
  }

  .charset {
    font-size: 13px;
    color: rgba(138, 138, 138, 1);
    float: left;
    height: 20px;
    display: block;
    float: left;
    text-align: center;
    margin-right: 20px;
    font-weight: 600;
  }

  .shape-together {
    min-width: 40%;
    height: 20px;
    float: left;
    position: relative;
  }

  .circle {
    width: 15px;
    height: 15px;
    float: left;
    margin-top: 2px;
  }

  .line {
    width: 100%;
    height: 1px;
    background-color: rgba(189, 189, 189, 0.19);
    overflow: hidden;
    position: absolute;
    top: 50%;
    left: 15px;
  }

  .user {
    margin-top: 30px;
    width: 100%;
    min-height: 140px;
  }

  .user-icon {
    float: left;
    width: 25%;
    height: 100px;
  }

  .user-message {
    width: 74%;
    float: left;
  }

  .icon {
    width: 59px;
    height: 59px;
  }

  .row1 p {
    font-size: 18px;
    color: rgba(62, 62, 62, 1);
    letter-spacing: 1px;
  }

  .row2 p, .row3 p {
    font-size: 12px;
    font-family: NotoSansHans-Regular;
    color: rgba(62, 62, 62, 1);
    min-height: 12px;
    padding: 13px 0;
  }

  .row2 {
    border-top: 1px solid rgba(221, 221, 221, 1);
    border-bottom: 1px solid rgba(221, 221, 221, 1);
  }

  .col {
    width: 100%;
    min-height: 170px;
    margin-bottom: 15px;
  }

  .col li {
    display: block;
    width: 25%;
    margin: 0 1%;
    min-height: 165px;
    float: left;
    background: url("./images/image-label.png") no-repeat center center;
    background-size: 100% 100%;
    list-style: none;
    text-align: center;
    padding: 0 3%;
    overflow: hidden;
  }

  .col1 {
    width: 100%;
    min-height: 20px;
    margin-bottom: 18px;
  }

  .menu {
    height: 80px;
    width: 100%;
  }

  .xi {
    height: 45px;
    font-size: 14px;
    font-family: NotoSansHans-Bold;
    color: rgba(51, 51, 50, 1);
    line-height: 45px;
  }

  .star {
    height: 30px;
    padding: 7px 0;
  }

  .star li {
    float: left;
  }

  .star li img {
    width: 23px;
    height: 23px;
  }

  .Permit {
    width: 96%;
    height: 125px;
    background-color: rgba(255, 229, 167, 1);
    margin-top: 20px;
    padding: 0 2%;
    border-radius: 4px;
  }

  .footer {
    width: 100%;
    height: 300px;
    text-align: center;
    margin-top: 20px;
  }

  .hehe {
    width: 17px;
    height: 17px;
    border: 1px solid black;
    border-radius: 9px;
    background: url("./images/icon-quotes.png") no-repeat center center;
    background-size: 8px 5px;
    margin: 0 auto;
    margin-top: 10px;
    margin-bottom: 10px;
  }

  .code {
    width: 141px;
    height: 141px;
    background-color: rgba(183, 183, 183, 1);
    margin: 0 auto;
  }

  .pp {
    font-size: 12px;
    min-height: 18px;
    padding-top: 6px;
    margin-top: 28px;
    border-bottom: 1px solid #ccc;
    font-weight: 600;
    background: url("./images/icon-quotes.png") no-repeat top right;
    width: 100%;
  }

  .bb {
    font-size: 10px;
    word-break: break-all;
    height: 66px;
    display: block;
    text-overflow: ellipsis;
    padding: 3px 0;
  }
  .Permit h2{
    color: rgba(51,51,50,1);
    font-size: 13px;
    padding: 6px 0;
  }
  .Permit p{
  color: rgba(110,106,97,1);
    font-size: 12px;
    padding: 10px 0;
    border-bottom: 1px dotted #ccc;
  }
  .Permit span{
  color: rgba(110,106,97,1);
    float: right;
    font-size: 12px;
  }
</style>
