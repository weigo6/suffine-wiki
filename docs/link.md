<div class="post-body">
  <div id="links">
    <style>
      /* 用于大屏幕和小屏幕的通用样式 */
      #links {
        display: flex; /* 使用 Flexbox 布局 */
        flex-wrap: wrap; /* 允许卡片换行 */
        justify-content: space-between; /* 卡片之间保持间距 */
      }
      .card {
        width: 45%;
        font-size: 1rem;
        padding: 10px 20px;
        border-radius: 4px;
        transition-duration: 0.15s;
        margin-bottom: 1rem;
        display: flex;
      }
      .card:hover {
        transform: scale(1.1);
        box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.12), 0 0 6px 0 rgba(0, 0, 0, 0.04);
      }
      .card a {
        border: none;
      }
      .card .ava {
        width: 3rem !important;
        height: 3rem !important;
        margin: 0 !important;
        margin-right: 1em !important;
        border-radius: 4px;
      }
      .card .card-header {
        font-style: italic;
        overflow: hidden;
        width: 100%;
      }
      .card .card-header a {
        font-style: normal;
        color: #608dbd;
        font-weight: bold;
        text-decoration: none;
      }
      .card .card-header a:hover {
        color: #d480aa;
        text-decoration: none;
      }
      .card .card-header .info {
        font-style: normal;
        color: #a3a3a3;
        font-size: 14px;
        min-width: 0;
        overflow: hidden;
        white-space: nowrap;
      }
      /* 媒体查询：小屏幕 */
      @media (max-width: 768px) {
        .card {
          width: 100%; /* 在小屏幕上显示为单列 */
        }
      }
    </style>
        <div class="card">
          <img class="ava" src="https://pic4.zhimg.com/80/v2-a0456a5f527c1923f096759f2926012f_1440w.webp" /> 
          <div class="card-header">
            <div>
              <a href="https://wcowin.work/ " target="_blank">Wcowin’s Web</a>
            </div>
            <div class="info">循此苦旅，以达星辰</div>
          </div>
        </div>
        <div class="card">
          <img class="ava" src="https://picbox.rutno.com/uploads/68444edfa6c4c.png" /> 
          <div class="card-header">
            <div>
              <a href="https://resume-github.netlify.app/" target="_blank">Resume-github</a>
            </div>
            <div class="info">电子名片 Demo</div>
          </div>
        </div>
  </div>
</div>