<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>SNS 로그인 설정</h1>
            <p>소셜로그인을 사용 여부를 설정 합니다.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                SNS 로그인 사용여부
              </div>
              <div class="item-option-340">
                  <input type='radio' name='whether' value='webopen' id="webopen" v-model="selectedSns" /> <label for="webopen" title="사용">사용</label>&emsp;
                  <input type='radio' name='whether' value='preparing' id="preparing" v-model="selectedSns" checked /> <label for="preparing" title="미사용">미사용</label>&emsp;
              </div>
              <div class="item-text">
                <p>· 소셜로그인을 사용 시 활성 키값을 입력하세요.</p>
              </div>
            </div>
          </div>

        </div>
      </div>

      <div class="option-grid" v-if="selectedSns === 'webopen'">
        <div class="option">
          <div class="option-title">
            <h1>SNS 정보설정</h1>
            <p>사이트 정보와 관련된 기본적인 설정을 합니다.  검색엔진 최적화를 위해 사이트 설명을 입력해주세요.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                네이버 로그인 설정
              </div>
              <div class="item-option-340">
                <input type='checkbox' id="client-check" name='client-check' v-model="isGoogleLoginEnabled" />
                <label for="client-check">네이버 로그인을 사용합니다.</label>
              </div>
               <div class="item-text">
                <p>· 네이버 CallbackURL&emsp;I&emsp;http://shoptp15.maxidc.net/plugin/social/?hauth.done=naver</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-id">네이버 Client ID</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-id' id="client-id" :disabled="!isGoogleLoginEnabled" value="" placeholder="" />
              </div>
              <button class="option-btn-s" v-if="isGoogleLoginEnabled">
                <a href="https://developers.naver.com/apps/#/register" target="_blank">앱 등록하기</a>
              </button>
              <button class="option-btn-s-disabled" v-else disabled>앱 등록하기</button>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-secret">네이버 Client Secret</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-secret' id="client-secret" :disabled="!isGoogleLoginEnabled" value="" placeholder="" />
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                카카오 로그인 설정
              </div>
              <div class="item-option-340">
                <input type='checkbox' id="client-check2" name='client-check2' v-model="isGoogleLoginEnabled2" />
                <label for="client-check2">카카오 로그인을 사용합니다.</label>
              </div>
               <div class="item-text">
                <p>· 카카오 CallbackURL&emsp;I&emsp;http://shoptp15.maxidc.net/plugin/social/?hauth.done=kakao</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-id">카카오 Client ID</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-id' id="client-id" :disabled="!isGoogleLoginEnabled2" value="" placeholder="" />
              </div>
              <button class="option-btn-s" v-if="isGoogleLoginEnabled2">
                <a href="https://developers.kakao.com/product/kakaoLogin" target="_blank">앱 등록하기</a>
              </button>
              <button class="option-btn-s-disabled" v-else disabled>앱 등록하기</button>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-secret">카카오 Client Secret</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-secret' id="client-secret" :disabled="!isGoogleLoginEnabled2" value="" placeholder="" />
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                페이스북 로그인 설정
              </div>
              <div class="item-option-340">
                <input type='checkbox' id="client-check3" name='client-check3' v-model="isGoogleLoginEnabled3" />
                <label for="client-check3">페이스북 로그인을 사용합니다.</label>
              </div>
               <div class="item-text">
                <p>· 페이스북 CallbackURL&emsp;I&emsp;http://shoptp15.maxidc.net/plugin/social/?hauth.done=facebook</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-id">페이스북 Client ID</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-id' id="client-id" :disabled="!isGoogleLoginEnabled3" value="" placeholder="" />
              </div>
              <button class="option-btn-s" v-if="isGoogleLoginEnabled3">
                <a href="https://developers.facebook.com/apps" target="_blank">앱 등록하기</a>
              </button>
              <button class="option-btn-s-disabled" v-else disabled>앱 등록하기</button>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-secret">페이스북 Client Secret</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-secret' id="client-secret" :disabled="!isGoogleLoginEnabled3" value="" placeholder="" />
              </div>
            </div>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                구글 로그인 설정
              </div>
              <div class="item-option-340">
                <input type="checkbox" id="client-check4" name="client-check4" v-model="isGoogleLoginEnabled4" />
                <label for="client-check4">구글 로그인을 사용합니다.</label>
              </div>
               <div class="item-text">
                <p>· 구글 CallbackURL&emsp;I&emsp;http://shoptp15.maxidc.net/plugin/social/?hauth.done=google</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-id">구글 Client ID</label>
              </div>
              <div class="item-option-340">
                <input type="text" name="client-id" id="client-id" :disabled="!isGoogleLoginEnabled4" value="" placeholder="" />
              </div>
              <button class="option-btn-s" v-if="isGoogleLoginEnabled4">
                <a href="https://console.cloud.google.com/apis/dashboard?pli=1&project=imweb-1576574511908" target="_blank">앱 등록하기</a>
              </button>
              <button class="option-btn-s-disabled" v-else disabled>앱 등록하기</button>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="client-secret">구글 Client Secret</label>
              </div>
              <div class="item-option-340">
                <input type='text' name='client-secret' id="client-secret" :disabled="!isGoogleLoginEnabled4" value="" placeholder="" />
              </div>
            </div>
          </div>

        </div>
      </div>

      <div class="page-btn">
        <button class="btn-save" title="저장하기">저장하기</button>
        <router-link to="/admin/dashboard/hosting"><button class="btn-next" title="다음으로">다음으로</button></router-link>
      </div>
    </form>

  </div>
</template>

<script>

export default {
  name: "snslogin",
  layout: "admin",
  data: () => ({
    isGoogleLoginEnabled: false,
    isGoogleLoginEnabled2: false,
    isGoogleLoginEnabled3: false,
    isGoogleLoginEnabled4: false,
    selectedSns : 'preparing',
  }),

}
</script>


