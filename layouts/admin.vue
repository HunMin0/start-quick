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
                  :title="list.title"
                  >{{list.title}}
                </router-link>
              </ul>
          </nav>
      </header>
      <section class="admin-section">
        <aside class="admin-aside">
          <div class="site-user">
            <h1><i class="fa-solid fa-circle-user"></i> &nbsp;퀵스타트 관리자</h1>
            <p>(1.0.0 ver 기준)</p>
          </div>
          <nav class="nav-side">
            <ul v-if="$route.path.includes('/admin/design')">
            <router-link
                  v-for="list in design_lists"
                  :key="list.key"
                  :to="list.link"
                  tag="li"
                  class="header-menu-list"
                  class-active="active"
                  :title="list.title"
                  exact><i :class="list.icon"></i>&emsp;{{list.title}}
                </router-link>
            </ul>
            <ul v-else>
              <router-link
                v-for="list in dash_lists"
                :key="list.key"
                :to="list.link"
                tag="li"
                class="header-menu-list"
                class-active="active"
                :title="list.title"
                exact><i :class="list.icon"></i>&emsp;{{list.title}}
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
        {link: '/admin/dashboard', title: '대시보드'},
        {link: '/admin/design', title: '디자인관리'},
        {link: '/admin/statistics', title: '통계'},
        {link: '/admin/setting', title: '환경설정'},
      ],
      dash_lists: [
        {link: '/admin/dashboard', title: '대시보드', icon: 'fa-solid fa-tv'},
        {link: '/admin/dashboard/popup', title: '팝업/배너 설정', icon: 'fa-solid fa-table-columns'},
        {link: '/admin/dashboard/homepage', title: '홈페이지 설정', icon: 'fa-solid fa-chart-gantt'},
        {link: '/admin/dashboard/snslogin', title: 'SNS 로그인 설정', icon: 'fa-solid fa-toggle-off'},
        {link: '/admin/dashboard/hosting', title: '호스팅/도메인 관리', icon: 'fa-regular fa-clipboard'},
        {link: '/admin/dashboard/terms', title: '약관 및 개인정보 설정', icon: 'fa-regular fa-file-lines'},
      ],
      design_lists: [
        {link: '/admin/design', title: '레이아웃 스타일', icon: 'fa-solid fa-tv'},
        {link: '/admin/design/logoset', title: '로고/파비콘/썸네일', icon: 'fa-solid fa-table-columns'},
        {link: '/admin/design/menuset', title: '메뉴 스타일', icon: 'fa-solid fa-chart-gantt'},
        {link: '/admin/design/visualset', title: '비주얼 스타일', icon: 'fa-solid fa-toggle-off'},
        {link: '/admin/design/sectionset', title: '섹션 컨텐츠', icon: 'fa-regular fa-clipboard'},
        {link: '/admin/design/footerset', title: '하단(푸터)', icon: 'fa-regular fa-file-lines'},
      ],
    }
  },
};

</script>
