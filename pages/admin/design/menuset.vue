<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>메뉴 스타일</h1>
            <p>홈페이지 상단 메뉴 스타일을 설정 합니다.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">레이아웃 형태</label>
              </div>
              <div class="item-columns">
                <div class="item-option3">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='leftMenu' id="leftMenu" checked /> <label for="leftMenu" title="좌측정렬">좌측정렬</label>
                  </div>
                  <div class="menu-layout-items1">
                    <div class="menu-type">
                      <div class="logo-area">
                        <p>로고영역</p>
                      </div>
                      <div class="menu-area">
                        <p>메뉴영역</p>
                      </div>
                    </div>
                    <div class="content-area">
                      <p>컨텐츠 영역</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option3">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='rightMenu' id="rightMenu" /> <label for="rightMenu" title="메뉴정렬">메뉴정렬</label>
                  </div>
                  <div class="menu-layout-items2">
                    <div class="menu-type">
                      <div class="logo-area">
                        <p>로고영역</p>
                      </div>
                      <div class="menu-right">
                        <div class="menu-area">
                        <p>메뉴영역</p>
                      </div>
                      </div>
                    </div>
                    <div class="content-area">
                      <p>컨텐츠 영역</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option3">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='betweenMenu' id="betweenMenu" /> <label for="betweenMenu" title="양쪽정렬">양쪽정렬</label>
                  </div>
                  <div class="menu-layout-items3">
                    <div class="menu-type">
                      <div class="logo-area">
                        <p>로고영역</p>
                      </div>
                      <div class="menu-area">
                        <p>메뉴영역</p>
                      </div>
                    </div>
                    <div class="content-area">
                      <p>컨텐츠 영역</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option3">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='centerMenu' id="centerMenu" /> <label for="centerMenu" title="가운데정렬">가운데정렬</label>
                  </div>
                  <div class="menu-layout-items4">
                    <div class="menu-type">
                      <div class="logo-area">
                        <p>로고영역</p>
                      </div>
                      <div class="menu-area">
                        <p>메뉴영역</p>
                      </div>
                    </div>
                    <div class="content-area">
                      <p>컨텐츠 영역</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option3">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='aroundMenu' id="aroundMenu" /> <label for="aroundMenu" title="균등정렬">균등정렬</label>
                  </div>
                  <div class="menu-layout-items5">
                    <div class="menu-type">
                      <div class="logo-area">
                        <p>로고영역</p>
                      </div>
                      <div class="menu-area">
                        <p>메뉴영역</p>
                      </div>
                    </div>
                    <div class="content-area">
                      <p>컨텐츠 영역</p>
                    </div>
                  </div>
                </div>
              </div>



            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                메뉴폰트 사이즈
              </div>
              <div class="item-option">
                  <input type='radio' name='fontsize' v-model="selectedFontSize" value='14px' id="14px"/> <label for="14px" title="14px">14px</label>&emsp;
                  <input type='radio' name='fontsize' v-model="selectedFontSize" value='15px' id="15px" checked/> <label for="15px" title="15px">15px(기본)</label>&emsp;
                  <input type='radio' name='fontsize' v-model="selectedFontSize" value='16px' id="16px"/> <label for="16px" title="16px">16px</label>&emsp;
                  <input type='radio' name='fontsize' v-model="selectedFontSize" value='user-click' id="user-click"/> <label for="user-click" title="직접입력">직접입력</label>&emsp;
                  <div class="bind-set" v-if="selectedFontSize === 'user-click'">
                    <div class="custom-input">
                      <input type='text' name='fontsize' value='' placeholder="숫자만 입력"/>&emsp;px
                    </div>
                  </div>
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                메뉴폰트 기본 색상
              </div>
              <div class="item-option">
                  <input type='radio' name='menuColor' v-model="selectedMenuColor" value='white' id="white" checked/> <label for="white" title="검은색(기본)">검은색(기본)</label>&emsp;
                  <input type='radio' name='menuColor' v-model="selectedMenuColor" value='black' id="black"/> <label for="black" title="흰색">흰색</label>&emsp;
                  <input type='radio' name='menuColor' v-model="selectedMenuColor" value='usercustom' id="usercustom"/> <label for="usercustom" title="직접입력">직접입력</label>&emsp;

                  <div class="bind-set" v-if="selectedMenuColor === 'usercustom'">
                    <input type="color" v-model="selectedMenuColor1">
                    <div class="custom-input">
                      <input type='text' name='menuColor' v-model="selectedMenuColor1" />
                    </div>
                  </div>

              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">메뉴 오버시 스타일</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='leftMenu' id="leftMenu" checked /> <label for="leftMenu" title="메뉴 색상변경(기본)">메뉴 색상변경(기본)</label>
                  </div>
                  <div class="menu-layout-items6">
                    <div class="menu-type">
                      <ul>
                        <li>메뉴1</li>
                        <li class="active1">메뉴2</li>
                        <li>메뉴3</li>
                        <li>메뉴4</li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='leftMenu' id="leftMenu" /> <label for="leftMenu" title="메뉴 밑줄적용">메뉴 밑줄적용</label>
                  </div>
                  <div class="menu-layout-items6">
                    <div class="menu-type">
                      <ul>
                        <li>메뉴1</li>
                        <li class="active2">메뉴2</li>
                        <li>메뉴3</li>
                        <li>메뉴4</li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>

              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='menulayout' value='leftMenu' id="leftMenu" /> <label for="leftMenu" title="메뉴 배경전환">메뉴 배경전환</label>
                  </div>
                  <div class="menu-layout-items6">
                    <div class="menu-type">
                      <ul>
                        <li>메뉴1</li>
                        <li class="active3">메뉴2</li>
                        <li>메뉴3</li>
                        <li>메뉴4</li>
                      </ul>
                    </div>
                  </div>
                </div>
              </div>

            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                오버시 폰트 색상
              </div>
              <div class="item-option-340">
                  <input type='radio' name='layoutcolor2' v-model="selectedPoint2" value='noncolor' id="noncolor" checked/> <label for="noncolor" title="검은색(기본)">검은색(기본)</label>&emsp;
                  <input type='radio' name='layoutcolor2' v-model="selectedPoint2" value='noncolor' id="noncolor" /> <label for="noncolor" title="흰색">흰색</label>&emsp;
                  <input type='radio' name='layoutcolor2' v-model="selectedPoint2" value='usercustom2' id="usercustom2"/> <label for="usercustom2" title="직접입력">직접입력</label>&emsp;

                  <div class="bind-set" v-if="selectedPoint2 === 'usercustom2'">
                    <input type="color" v-model="selectedColor2">
                    <div class="custom-input">
                      <input type='text' name='layoutcolor2' v-model="selectedColor2" />
                    </div>
                  </div>
              </div>
              <div class="item-title3">
                오버시 밑줄색상
              </div>
              <div class="item-option">
                  <input type='radio' name='layoutcolor3' v-model="selectedPoint3" value='noncolor' id="noncolor" checked/> <label for="noncolor" title="검은색(기본)">검은색(기본)</label>&emsp;
                  <input type='radio' name='layoutcolor3' v-model="selectedPoint3" value='noncolor' id="noncolor" /> <label for="noncolor" title="흰색">흰색</label>&emsp;
                  <input type='radio' name='layoutcolor3' v-model="selectedPoint3" value='usercustom3' id="usercustom3"/> <label for="usercustom3" title="직접입력">직접입력</label>&emsp;
                  <div class="bind-set" v-if="selectedPoint3 === 'usercustom3'">
                    <input type="color" v-model="selectedColor3">
                    <div class="custom-input">
                      <input type='text' name='layoutcolor3' v-model="selectedColor3" />
                    </div>
                  </div>
              </div>
            </div>
          </div>

        </div>
      </div>



      <div class="page-btn">
        <button class="btn-save" title="저장하기">저장하기</button>
        <router-link to="/admin/design/logoset"><button class="btn-next" title="다음으로">다음으로</button></router-link>
      </div>
    </form>
  </div>
</template>

<script>

export default {
  name: "menuset",
  layout: "admin",
  data: () => ({
    selectedColor: '#111111',
    selectedMenuColor1: '#111111',
    selectedColor2: '#111111',
    selectedColor3: '#111111',
    selectedLayoutSize: 'px1250',
    selectedMenuColor: 'white',
    selectedPoint2: 'noncolor',
    selectedPoint3: 'noncolor',
    selectedFontSize: '15px',

    checkTemplate1: true,
    checkTemplate2: false,
    checkTemplate3: false,
    template: 'basic',
  }),

}
</script>
