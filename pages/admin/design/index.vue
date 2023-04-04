<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>템플릿 스타일</h1>
            <p>입력하신 정보는 홈페이지 하단의 카피라이터에 적용 됩니다.</p>
            <div class="option-right-btn">
              <button class="option-btn-s">템플릿 업로드</button>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-option-template">
                <div class="template-form">
                  <div class="template-items">
                    <div class="template-img">
                      <p>기본 베이직 레이아웃</p>
                    </div>
                    <div class="template-title item-option">
                      <input type='radio' name='template1' value='template1' id="template1" :checked="checkTemplate1" /> <label for="template1" title="접속허용">적용</label>&emsp;
                      <input type='radio' name='template1' value='notemplate1' id="notemplate1" :checked="!checkTemplate1" /> <label for="notemplate1" title="접속제한">미적용</label>
                    </div>
                  </div>
                  <div class="template-items">
                    <div class="template-img template_img1"></div>
                    <div class="template-title item-option">
                      <input type='radio' name='template2' value='template2' id="template2" :checked="checkTemplate2" /> <label for="template2" title="접속허용">적용</label>&emsp;
                      <input type='radio' name='template2' value='notemplate2' id="notemplate2" :checked="!checkTemplate2" /> <label for="notemplate2" title="접속제한">미적용</label>
                    </div>
                  </div>
                  <div class="template-items">
                    <div class="template-img template_img2"></div>
                    <div class="template-title item-option">
                      <input type='radio' name='template3' value='template3' id="template3" :checked="checkTemplate3" /> <label for="template3" title="접속허용">적용</label>&emsp;
                      <input type='radio' name='template3' value='notemplate3' id="notemplate3" :checked="!checkTemplate3" /> <label for="notemplate3" title="접속제한">미적용</label>
                    </div>
                  </div>
                  <div class="template-items">
                    <div class="template-img template_img3"></div>
                    <div class="template-title item-option">
                      <input type='radio' name='template4' value='template4' id="template4" /> <label for="template4" title="접속허용">적용</label>&emsp;
                      <input type='radio' name='template4' value='notemplate4' id="notemplate4" checked/> <label for="notemplate4" title="접속제한">미적용</label>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>레이아웃 스타일</h1>
            <p>입력하신 정보는 홈페이지 하단의 카피라이터에 적용 됩니다.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">레이아웃 형태</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout' value='fullpage' id="fullpage" /> <label for="fullpage" title="풀페이지">풀페이지</label>
                  </div>
                  <div class="page-layout-items1">
                    <p>컨텐츠 영역</p>
                  </div>
                </div>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout' value='pxpage' id="pxpage" checked/> <label for="pxpage" title="픽셀기준">픽셀기준</label>
                  </div>
                  <div class="page-layout-items2">
                    <p>컨텐츠 영역</p>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                레이아웃 형태
              </div>
              <div class="item-option">
                  <input type='radio' name='layoutsize' v-model="selectedLayoutSize" value='px1200' id="px1200"/> <label for="px1200" title="1200px">1200px</label>&emsp;
                  <input type='radio' name='layoutsize' v-model="selectedLayoutSize" value='px1250' id="px1250" checked/> <label for="px1250" title="1250px">1250px(기본)</label>&emsp;
                  <input type='radio' name='layoutsize' v-model="selectedLayoutSize" value='px1300' id="px1300"/> <label for="px1300" title="1300px">1300px</label>&emsp;
                  <input type='radio' name='layoutsize' v-model="selectedLayoutSize" value='px1350' id="px1350"/> <label for="px1350" title="1350px">1350px</label>&emsp;
                  <input type='radio' name='layoutsize' v-model="selectedLayoutSize" value='user-click' id="user-click"/> <label for="user-click" title="직접입력">직접입력</label>&emsp;
                  <div class="bind-set" v-if="selectedLayoutSize === 'user-click'">
                    <div class="custom-input">
                      <input type='text' name='layoutsize' value='' placeholder="숫자만 입력"/>&emsp;px
                    </div>
                  </div>
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                로그인 활성여부
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='toplayout' value='top-layout' id="top-layout" v-model="selectedToplogo" checked /> <label for="top-layout" title="미사용">미사용</label>&emsp;
                    <input type='radio' name='toplayout' value='top-layout-on' id="top-layout-on" v-model="selectedToplogo" /> <label for="top-layout-on" title="사용">사용</label>
                  </div>
                  <div class="page-layout-items3" v-if=" selectedToplogo === 'top-layout-on'">
                    <div></div>
                    <div></div>
                    <p>컨텐츠 영역</p>
                  </div>
                </div>
              </div>
              <div class="item-columns" v-if=" selectedToplogo === 'top-layout-on'">
                <div class="item-option">
                  <div class="option-select">
                    <div class="phrases-info">
                      로그인 여부 사용 시, 상단영역에 로그인 메뉴가 추가 됩니다.
                    </div>
                    <div class="phrases-info">
                      좌측 상단에 문구 혹은 이미지 등록
                    </div>
                    <div class="phrases">
                      <input type='text' name='left-phrases' value='' placeholder="입력하실 문구" />
                      <p>컬러값</p>
                      <div class="color-pick">
                        <input type="color" v-model="selectedColor">
                        <div class="custom-input">
                          <input type='text' name='layoutsize' value='' v-model="selectedColor" />
                        </div>
                      </div>
                    </div>
                    <div class="phrases">

                      <div class="filebox">
                        <input class="upload-name" value="" placeholder="png, jpg만 업로드 가능 합니다">
                        <label for="file">이미지 파일선택</label>
                        <input type="file" id="file">
                      </div>

                    </div>
                    <div class="item-text">
                      <p>· 권장 해상도 320px * 50px 기준</p>

                    </div>

                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                포인트 색상
              </div>
              <div class="item-option">
                  <input type='radio' name='layoutcolor' v-model="selectedPoint" value='white' id="white" checked/> <label for="white" title="흰색(기본)">흰색(기본)</label>&emsp;
                  <input type='radio' name='layoutcolor' v-model="selectedPoint" value='black' id="black"/> <label for="black" title="검은색">검은색</label>&emsp;
                  <input type='radio' name='layoutcolor' v-model="selectedPoint" value='usercustom' id="usercustom"/> <label for="usercustom" title="직접입력">직접입력</label>&emsp;

                  <div class="bind-set" v-if="selectedPoint === 'usercustom'">
                    <input type="color" v-model="selectedColor1">
                    <div class="custom-input">
                      <input type='text' name='layoutcolor' v-model="selectedColor1" />
                    </div>
                  </div>

              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                포인트 서브색상 1
              </div>
              <div class="item-option-340">
                  <input type='radio' name='layoutcolor2' v-model="selectedPoint2" value='noncolor' id="noncolor" checked/> <label for="noncolor" title="없음">없음</label>&emsp;
                  <input type='radio' name='layoutcolor2' v-model="selectedPoint2" value='usercustom2' id="usercustom2"/> <label for="usercustom2" title="직접입력">직접입력</label>&emsp;

                  <div class="bind-set" v-if="selectedPoint2 === 'usercustom2'">
                    <input type="color" v-model="selectedColor2">
                    <div class="custom-input">
                      <input type='text' name='layoutcolor2' v-model="selectedColor2" />
                    </div>
                  </div>
              </div>
              <div class="item-title3">
                포인트 서브색상 2
              </div>
              <div class="item-option">
                  <input type='radio' name='layoutcolor3' v-model="selectedPoint3" value='noncolor' id="noncolor" checked/> <label for="noncolor" title="없음">없음</label>&emsp;
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
        <button class="btn-next" title="다음으로">다음으로</button>
      </div>
    </form>
  </div>
</template>

<script>

export default {
  name: "design",
  layout: "admin",
  data: () => ({
    selectedColor: '#111111',
    selectedColor1: '#111111',
    selectedColor2: '#111111',
    selectedColor3: '#111111',
    selectedToplogo: 'top-layout',
    selectedLayoutSize: 'px1250',
    selectedPoint: 'white',
    selectedPoint2: 'noncolor',
    selectedPoint3: 'noncolor',

    checkTemplate1: true,
    checkTemplate2: false,
    checkTemplate3: false
  }),
  mounted() {
    // template1가 체크되어 있는 경우
    if (document.getElementsByName('template1')[0].checked) {
      this.checkTemplate3 = false;
      this.checkTemplate2 = false;
    }
    // template2이 체크되어 있는 경우
    else if (document.getElementsByName('template2')[0].checked) {
      this.checkTemplate1 = false;
      this.checkTemplate3 = false;
    }
    // template3이 체크되어 있는 경우
    else if (document.getElementsByName('template3')[0].checked) {
      this.checkTemplate1 = false;
      this.checkTemplate2 = false;
    }
  }

}
</script>
