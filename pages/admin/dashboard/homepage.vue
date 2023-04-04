<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>기본설정</h1>
            <p>사이트 정보와 관련된 기본적인 설정을 합니다.  검색엔진 최적화를 위해 사이트 설명을 입력해주세요.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                사이트 오픈여부
              </div>
              <div class="item-option-340">
                  <input type='radio' name='whether' value='webopen' id="webopen"/> <label for="webopen" title="오픈">오픈</label>&emsp;
                  <input type='radio' name='whether' value='preparing' id="preparing" checked/> <label for="preparing" title="준비중">준비중</label>&emsp;
                  <input type='radio' name='whether' value='webopen' id="disabled" disabled> <label for="disabled" title="비활성">비활성</label>
              </div>
              <div class="item-text">
                <p>· 디자인등록이 완료되면 자동으로 오픈 처리가 되므로 반영이 필요치 않을 경우 준비중으로 변경 해주세요.</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="site-name">사이트 이름</label>
              </div>
              <div class="item-option-340">
                <input type='text' id="site-name" name='site-name' value='' placeholder="예) 홈페이지 이름"/>
              </div>
              <div class="item-text">
                <p>· 브라우저 탭이나 소셜 미디어에 공유할 때 표시됩니다.</p>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="site-subject">사이트 설명</label>
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

      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>홈페이지 정보</h1>
            <p>입력하신 정보는 홈페이지 하단의 카피라이터에 적용 됩니다.</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                <label for="company-name">회사/단체명</label>
              </div>
              <div class="item-option2">
                <input type='text' id="company-name" name='company-name' value='' placeholder="회사명 입력" class="inp-w260"/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="company-ceo">대표자 이름</label>
              </div>
              <div class="item-option2">
                <input type='email' id="company-ceo" name='company-ceo' value='' placeholder="대표자명 입력"/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="company-email">대표 메일</label>
              </div>
              <div class="item-option2">
                <input type='text' id="company-email" name='company-email' value='' placeholder="대표메일 입력"/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                주소
              </div>
              <div class="item-option2">
                <input type='text' name='company-address' value='' placeholder="주소를 검색해주세요" disabled/>
              </div>
              <button class="option-btn-s">검색</button>&emsp;
              <div class="item-title2">
                상세주소
              </div>
              <div class="item-option-340">
                <input type='text' name='company-address2' value='' placeholder="상세주소 입력" />
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                우편번호
              </div>
              <div class="item-option2">
                <input type='number' name='zip-code' value='' placeholder="예) 12345" min="1" max="99999"/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="company-number">사업자등록번호</label>
              </div>
              <div class="item-option2">
                <input type='text' id="company-number" name='company-number' value='' placeholder="예) 123-45-67891"/>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="company-number2">통신판매업신고번호</label>
              </div>
              <div class="item-option2">
                <input type='text' id="company-number2" name='company-number2' value='' placeholder="예) 2023-OOOO-1234"/>
              </div>
            </div>

          </div>

        </div>
      </div>

      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>메타태그</h1>
            <p>추가로 사용하실 meta 태그를 입력합니다.</p>
          </div>

          <div class="option-setting">
            <div class="option-items2">
              <div class="item-title">
                <label for="mata-tag">추가 메타태그</label>
              </div>
              <div class="item-option">
                <textarea name="mata-tag" id="mata-tag" cols="30" rows="10" placeholder="추가로 사용하실 meta 태그를 입력합니다."></textarea>
              </div>
            </div>

          </div>

        </div>
      </div>

      <div class="page-btn">
        <button class="btn-save" title="저장하기">저장하기</button>
        <router-link to="/admin/dashboard/snslogin"><button class="btn-next" title="다음으로">다음으로</button></router-link>
        <button class="btn-disble" title="비활성상태" disabled>비활성상태</button>
      </div>
    </form>

  </div>
</template>

<script>

export default {
  name: "homepage",
  layout: "admin",
  data: () => ({

  }),

}
</script>


