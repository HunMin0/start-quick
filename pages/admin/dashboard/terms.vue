<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>이용약관</h1>
            <p> 이용약관 URL&emsp;I&emsp;http://webtp.maxidc.com/?mode=policy</p>
          </div>

          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                이용약관
              </div>
              <div class="item-option-340">
                  <input type='radio' name='whether' value='webopen' id="webopen"/> <label for="webopen" title="사용">사용</label>&emsp;
                  <input type='radio' name='whether' value='preparing' id="preparing" checked/> <label for="preparing" title="미사용">미사용</label>&emsp;
              </div>
            </div>
          </div>

        </div>
      </div>

      <div class="page-btn">
        <button class="btn-save" title="저장하기">저장하기</button>
        <button class="btn-next" title="다음으로">다음으로</button>
        <button class="btn-disble" title="비활성상태" disabled>비활성상태</button>
      </div>
    </form>
  </div>
</template>

<script>

export default {
  name: "terms",
  layout: "admin",
  data: () => ({

  }),

}
</script>


