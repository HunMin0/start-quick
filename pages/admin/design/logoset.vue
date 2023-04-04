<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>로고 설정</h1>
            <p>등록하신 로고는 홈페이지 메인로고에 사용 됩니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">로고등록</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout' value='logoimg' id="logoimg" v-model="selectedLogo" checked /> <label for="logoimg" title="이미지 사용">이미지 사용</label>&emsp;
                    <input type='radio' name='weblayout' value='logotext' id="logotext" v-model="selectedLogo" /> <label for="logotext" title="텍스트 사용">텍스트 사용</label>
                  </div>
                  <div class="web-logo" v-if="selectedLogo === 'logoimg'">
                    <div class="filebox">
                      <input class="upload-name" value="" placeholder="png, jpg만 업로드 가능 합니다">
                      <label for="file">이미지 파일선택</label>
                      <input type="file" id="file">
                      <div class="item-text">
                        <p>· 권장 해상도 400px * 80px 기준</p>
                      </div>
                    </div>
                    <div class="logo-sample">
                      <p>등록된 이미지</p>
                    </div>
                  </div>
                  <div class="web-logo" v-if="selectedLogo === 'logotext'">
                    <div class="item-option-reset">
                    <div class="option-select">
                      <div class="phrases">
                        <input type='text' name='left-phrases' value='' placeholder="회사명 및 로고명" />
                        <p>컬러값</p>
                        <div class="color-pick">
                          <input type="color" v-model="selectedColor">
                          <div class="custom-input">
                            <input type='text' name='layoutsize' value='' v-model="selectedColor" />
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                    <div class="logo-sample">
                      <p>등록된 로고명</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">하단 로고등록</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout2' value='nologo' id="nologo" v-model="selectedFotterLogo" checked /> <label for="nologo" title="미등록">미등록</label>&emsp;
                    <input type='radio' name='weblayout2' value='logoimg2' id="logoimg2" v-model="selectedFotterLogo" /> <label for="logoimg2" title="이미지 사용">이미지 사용</label>&emsp;
                    <input type='radio' name='weblayout2' value='logotext2' id="logotext2" v-model="selectedFotterLogo" /> <label for="logotext2" title="텍스트 사용">텍스트 사용</label>
                  </div>
                </div>
                <div class="item-columna" v-if="selectedFotterLogo === 'nologo'">
                  <div class="item-option">
                    <div class="item-text">
                      <p>· 하단 카피라이터 부분에 적용됩니다. 미등록시 기본 로고 정보를 사용 합니다.</p>
                    </div>
                  </div>
                </div>
                <div class="item-columnn" v-if="selectedFotterLogo === 'logoimg2'">
                   <div class="item-option">
                    <div class="web-logo">
                      <div class="filebox">
                        <input class="upload-name" value="" placeholder="png, jpg만 업로드 가능 합니다">
                        <label for="file">이미지 파일선택</label>
                        <input type="file" id="file">
                      </div>
                    </div>
                    <div class="item-text">
                      <p>· 권장 해상도: 240x90 / PNG,JPG</p>
                    </div>
                  </div>
                </div>
                <div class="item-columna" v-if="selectedFotterLogo === 'logotext2'">
                  <div class="item-option">
                    <div class="option-select">
                      <div class="phrases">
                        <input type='text' name='left-phrases' value='' placeholder="회사명 및 로고명" />
                        <p>컬러값</p>
                        <div class="color-pick">
                          <input type="color" v-model="selectedColor">
                          <div class="custom-input">
                            <input type='text' name='layoutsize' value='' v-model="selectedColor" />
                          </div>
                        </div>
                      </div>
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
            <h1>파비콘 설정</h1>
            <p>웹사이트를 볼 때 브라우저 탭에 표시되는 아이콘입니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">파비콘 등록</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout3' value='nofavicon' v-model="selectedFavicon" id="nofavicon" checked /> <label for="nofavicon" title="미등록">미등록</label>&emsp;
                    <input type='radio' name='weblayout3' value='pngfavicon' v-model="selectedFavicon" id="pngfavicon" /> <label for="pngfavicon" title="PNG 등록">PNG 등록</label>&emsp;
                    <input type='radio' name='weblayout3' value='icofavicon' v-model="selectedFavicon" id="icofavicon" /> <label for="icofavicon" title="ICO 등록">ICO 등록</label>
                  </div>
                </div>
                <div class="item-columnn" v-if="selectedFavicon === 'pngfavicon'">
                  <div class="item-option">
                    <div class="web-logo">
                      <div class="filebox">
                        <input class="upload-name" value="" placeholder="png, jpg만 업로드 가능 합니다">
                        <label for="file">이미지 파일선택</label>
                        <input type="file" id="file">
                      </div>
                    </div>
                    <div class="item-text">
                      <p>· 권장 해상도: 512x512 / PNG</p>
                    </div>
                  </div>
                </div>
                <div class="item-columnn" v-if="selectedFavicon === 'icofavicon'">
                  <div class="item-option">
                    <div class="web-logo">
                      <div class="filebox">
                        <input class="upload-name" value="" placeholder="ICO만 업로드 가능 합니다">
                        <label for="file">이미지 파일선택</label>
                        <input type="file" id="file">
                      </div>
                    </div>
                    <div class="item-text">
                      <p>· 권장 해상도: 512x512 / ICO</p>
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
            <h1>썸네일 설정</h1>
            <p>카카오톡 공유시 나타나는 홈페이지 썸네일 이미지를 등록 합니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">썸네일 등록</label>
              </div>
              <div class="item-columns">
                <div class="item-option">
                  <div class="option-select">
                    <input type='radio' name='weblayout4' value='nokakaoimg' id="nokakaoimg" v-model="selectedKakao" checked /> <label for="nokakaoimg" title="미등록">미등록</label>&emsp;
                    <input type='radio' name='weblayout4' value='kakaoimg' id="kakaoimg" v-model="selectedKakao" /> <label for="kakaoimg" title="이미지 등록">이미지 등록</label>
                  </div>
                </div>
                <div class="item-columnn" v-if="selectedKakao === 'kakaoimg'">
                  <div class="item-option">
                    <div class="web-logo">
                      <div class="filebox">
                        <input class="upload-name" value="" placeholder="png, jpg만 업로드 가능 합니다">
                        <label for="file">이미지 파일선택</label>
                        <input type="file" id="file">
                      </div>
                    </div>
                    <div class="item-text">
                      <p>· 권장 해상도: 512x512 / PNG</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="option-setting" v-if="selectedKakao === 'kakaoimg'">
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">썸네일 안내문구</label>
              </div>
              <div class="item-columns">
                <div class="item-option-340">
                  <input type='text' id="site-name" name='site-name' value='' placeholder="안내문구를 입력하세요."/>
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
  name: "logoset",
  layout: "admin",
  data: () => ({
    selectedColor: '#111111',
    selectedColor1: '#111111',
    selectedColor2: '#111111',
    selectedColor3: '#111111',
    selectedLogo : 'logoimg',
    selectedFotterLogo : 'nologo',
    selectedFavicon: 'nofavicon',
    selectedKakao: 'nokakaoimg',
  }),

}
</script>
