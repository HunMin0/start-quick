<template>
  <div>
    <form action='#'>
      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>템플릿 스타일</h1>
            <p>입력하신 정보는 홈페이지 하단의 카피라이터에 적용 됩니다.</p>
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
                      <input type='radio' name='connect' value='permit' id="permit" checked/> <label for="permit" title="접속허용">적용</label>&emsp;
                      <input type='radio' name='connect' value='nopermit' id="nopermit" /> <label for="nopermit" title="접속제한">미적용</label>&emsp;
                    </div>
                  </div>

                  <div class="template-items">
                    <div class="template-img">a</div>
                    <div class="template-title">a</div>
                  </div>
                  <div class="template-items">
                    <div class="template-img">a</div>
                    <div class="template-title">a</div>
                  </div>
                  <div class="template-items">
                    <div class="template-img">a</div>
                    <div class="template-title">a</div>
                  </div>
                </div>
              </div>
            </div>

          </div>

        </div>
      </div>

    </form>
  </div>
</template>

<script>

export default {
  name: "design",
  layout: "admin",
  data: () => ({

  }),

}
</script>


