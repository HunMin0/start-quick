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
               <router-link
                  v-for="list in dash_lists"
                  :key="list.key"
                  :to="list.link"
                  tag="li"
                  class="header-menu-list"
                  class-active="active"
                  exact>{{list.title}}
                </router-link>
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
        {link: '/statistics', title: '통계'},
        {link: '/setting', title: '환경설정'},
      ],
      dash_lists: [
        {link: '/admin', title: '대시보드'},
        {link: '/design', title: '팝업/배너 설정'},
        {link: '/sns', title: 'SNS 로그인 설정'},
        {link: '/hosting', title: '호스팅/도메인 관리'},
        {link: '/terms', title: '약관 및 개인정보 설정'},
      ],
    }
  }
}

</script>
