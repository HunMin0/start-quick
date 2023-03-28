<template>
  <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>도메인관리</h1>
            <p>외부 도메인 연결시 도메인 제공사에서 DNS정보를 변경해주세요.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                기본제공주소
              </div>
              <div class="item-option-340">
                webtp.maxidc.net
              </div>
              <div class="item-title">
                대표도메인
              </div>
              <div class="item-option-340">
                webtp.maxidc.net
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">연결할 도메인주소</label>
              </div>
              <div class="item-option-340">
                http://&emsp;<input type='text' id="site-name" name='site-name' value='' placeholder=""/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="site-subject">연결한 도메인</label>
              </div>
              <div class="item-option-340">
                <input type='text' id="site-subject" name='site-subject' value='' placeholder="예) 웹에이전시 전문 기업 입니다."/>
              </div>
              <div class="item-text">
                <p>· 사이트를 대표하는 문장이나 키워드를 사용하세요. 검색엔진 검색 결과에 반영됩니다.</p>
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
</template>

<script>

export default {
  name: "hosting",
  layout: "admin",
  data: () => ({

  }),

}
</script>


