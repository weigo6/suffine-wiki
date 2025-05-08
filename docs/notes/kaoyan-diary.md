---
title:  学习日记
hide:
    - footer # 隐藏翻页
comments: false  # 评论，默认不开启
tags: 
    - 一研为定
---
# 学习日记

## 凡是过往，皆为序章
一些碎碎念，打卡一下学习过程。

<body>
<center>
<font color="#4351AF" size=5 >
  <div id="countdown"></div>

  <script>
    // 设置倒计时时间为2025年12月20号结束
    var countDownDate = new Date("Dec 20, 2025 00:00:00").getTime();

    // 更新倒计时
    var x = setInterval(function() {
      // 获取当前时间
      var now = new Date().getTime();

      // 计算剩余时间
      var distance = countDownDate - now;

      // 计算天数、小时、分钟和秒
      var days = Math.floor(distance / (1000 * 60 * 60 * 24));
      var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      var seconds = Math.floor((distance % (1000 * 60)) / 1000);

      // 显示倒计时
      document.getElementById("countdown").innerHTML = days + "天 " + hours + "小时 "
      + minutes + "分钟 " + seconds + "秒";

      // 当倒计时结束时，停止更新
      if (distance < 0) {
        clearInterval(x);
        document.getElementById("countdown").innerHTML = "倒计时结束";
      }
    }, 1000);
  </script>
</font>
</center>
</body>

---

<!-- 授权码输入框，样式定义在extra.css中-->
<div id="auth-container">
  <input type="password" id="auth-input" placeholder="请输入授权码">
  <button onclick="verifyAuthCode()">验证</button>
</div>

<!-- 评论系统容器，初始隐藏 -->
<div id="comments-container" style="display: none;">
  <script id="giscus-script" src="https://giscus.app/client.js"
    data-repo="weigo6/suffine-giscus"
    data-repo-id="R_kgDOOlJ7eA"
    data-category="General"
    data-category-id="DIC_kwDOOlJ7eM4Cp0PV"
    data-mapping="pathname"
    data-strict="0"
    data-reactions-enabled="1"
    data-emit-metadata="0"
    data-input-position="bottom"
    data-theme="light" 
    data-lang="zh-CN"
    crossorigin="anonymous"
    async>
  </script>
</div>

<script>
  // 从 mkdocs 的 extra 中获取授权码
  const correctAuthCode = "{{ config.extra.comment_auth_code }}";
  function verifyAuthCode() {
    const inputCode = document.getElementById("auth-input").value;
    if (inputCode === correctAuthCode) {
      document.getElementById("auth-container").style.display = "none";
      document.getElementById("comments-container").style.display = "block";
    } else {
      alert("授权码错误，请重新输入。");
    }
  }
</script>