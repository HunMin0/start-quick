<template>
   <v-app>
    <div id="admin-default">
      <header class="admin-header">
          <div class="logo-top">
            <a href="/admin">Quick Start</a>
          </div>
          <nav class="nav-top">
              <ul>
                <router-link
                  v-for="list in lists"
                  :key="list.key"
                  :to="list.link"
                  tag="li"
                  class="header-menu-list"
                  class-active="active"
                  exact>{{list.title}}
                </router-link>
              </ul>
          </nav>
      </header>
      <section class="admin-section">
        <aside class="admin-aside">
          <div class="site-user">
            <h1>퀵스타트 관리자</h1>
            <p>(1.0.0 ver 기준)</p>
          </div>
          <nav class="nav-side">
            <ul>
              <li class="active">
                <a href="#none">
                  <img src="/" alt="" />대시보드</a>
              </li>
              <li>
                <a href="#none">팝업/배너 설정</a>
              </li>
              <li>
                <a href="#none">홈페이지 설정</a>
              </li>
              <li>
                <a href="#none">SNS 로그인 설정</a>
              </li>
              <li>
                <a href="#none">호스팅/도메인 관리</a>
              </li>
              <li>
                <a href="#none">약관 및 개인정보 설정</a>
              </li>
            </ul>
          </nav>
        </aside>
        <div class="admin-container">
          <div class="container-head">
              <div class="admin-inner">
                <div class="container-title">
                  <h1>퀵스타트 홈페이지</h1>
                  <p>대표도메인 : webtp.maxidc.net</p>
                </div>
                <div class="container-info">
                    <p>용량</p>
                    <div class="volume"></div>
                  <p><span>600mb</span> / 1G</p>
                </div>
              </div>
            </div>
            <div class="container-content">
              <div class="content-set">
                <div class="admin-inner">
                  <Nuxt />
                </div>
              </div>
              <footer>
                <div class="admin-inner">
                    Copyright © WEB 2023. All Rights Reserved.
                </div>
              </footer>
            </div>
        </div>
      </section>
     </div>
   </v-app>
</template>

<script>
export default {
  name: 'admin',
  data () {
    return {
      lists: [
        {link: '/admin', title: '대시보드'},
        {link: '/design', title: '디자인관리'},
        {link: '/sad', title: '통계'},
        {link: '/sads', title: '환경설정'},
      ]
    }
  }
}

</script>
