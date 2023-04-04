<template>
  <form action='#'>
    <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>호스팅관리</h1>
            <p>호스팅 사용내역을 조회 합니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                서비스 시작일
              </div>
              <div class="item-option-340">
                <p class="font-basic">2023-02-20</p>
              </div>
              <div class="item-title">
                서비스 만료일
              </div>
              <div class="item-option-340">
                <p class="font-basic">2023-02-20 <span class="font-delete">(364일 남음)</span></p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items3">
              <div class="item-title">
                디스크 사용량
              </div>
              <div class="item-option">
                <div class="hosting-progress">
                  <div class="warning">주의요망</div>
                  <ul class="progress-info">
                    <li>0</li>
                    <li>25</li>
                    <li>50</li>
                    <li>75</li>
                    <li>100</li>
                  </ul>
                  <div class="volume2"></div>
                </div>
                <p class="font-basic"><span class="font-main">46M(23%)</span> 사용중 / 총 200M</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items3">
              <div class="item-title">
                트래픽 사용량
              </div>
              <div class="item-option">
                <div class="hosting-progress">
                  <div class="warning">주의요망</div>
                  <ul class="progress-info">
                    <li>0</li>
                    <li>25</li>
                    <li>50</li>
                    <li>75</li>
                    <li>100</li>
                  </ul>
                  <div class="volume3"></div>
                </div>
                <p class="font-basic"><span class="font-main">22M(11%)</span> 사용중 / 총 300M</p>
              </div>
            </div>
          </div>
        </div>
      </div>

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
              <div class="item-column">
                <div class="item-row">
                   <div class="item-option-340">
                      http://&emsp;<input type='text' id="site-name" name='site-name' value='' placeholder=""/>&emsp;
                      <button class="option-btn-s">등록하기</button>
                    </div>
                    <div class="item-option">
                      <input type='checkbox' id="client-domain" name='client-domain' />
                      <label for="client-domain">대표도메인 설정</label>
                    </div>
                </div>
                <div class="item-row">
                    <div class="item-text-m">
                      <p>· 연결할 도메인주소에 'www'없이 추가하시기 바랍니다. 'www'가 자동으로 추가됩니다.</p>
                    </div>
                </div>
              </div>
            </div>
            <div class="option-items">
              <div class="item-title">
                <label for="site-subject">연결한 도메인</label>
              </div>
              <div class="item-column">
                <div class="item-row">
                  <div class="item-option">
                    <div class="item-option-domain">
                      <div><span>1.</span>&emsp;http://webtp.maxidc.net</div>
                      <p>등록일&emsp;<span>2023-00-00</span></p>
                      <div class="domain-btn">
                        <button class="option-btn-disabled">대표도메인 변경</button>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="item-row">
                  <div class="item-option">
                    <div class="item-option-domain">
                      <div><span>2.</span>&emsp;http://sample.co.kr</div>
                      <p>등록일&emsp;<span>2023-00-00</span></p>
                      <div class="domain-btn">
                        <button class="option-btn-s-dark">대표도메인 변경</button>
                        <button class="option-btn-s-delete">도메인 삭제</button>
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
            <h1>SSl관리</h1>
            <p>SSL정보를 확인 합니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                SSL 연결 상태
              </div>
              <div class="item-option-340">
                <p class="font-delete">미연결</p>
              </div>
              <div class="item-title">
                SSL 연결 도메인
              </div>
              <div class="item-option-340">
                <p class="font-disble">webtp.maxidc.net</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                SSL 시작일
              </div>
              <div class="item-option-340">
                <p class="font-disble">2023-00-00</p>
              </div>
              <div class="item-title">
                SSL 만료일
              </div>
              <div class="item-option-340">
                <p class="font-disble">2023-00-00</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>웹서버/FTP정보</h1>
            <p>호스팅 서버정보를 확인 합니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                웹서버 아이피
              </div>
              <div class="item-option-340">
                <p class="font-basic">112.175.184.61</p>
              </div>
              <div class="item-title">
                웹서버 정보
              </div>
              <div class="item-option-340">
                <p class="font-delete">Apache 2.4</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                PHP 버전
              </div>
              <div class="item-option-340">
                <p class="font-delete">PHP 7.4</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                홈 디렉토리
              </div>
              <div class="item-option-340">
                <p class="font-basic">/host/home1/khm10090</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                FTP 아이디
              </div>
              <div class="item-option-340">
                <p class="font-delete">khm10090</p>
              </div>
              <div class="item-title">
                FTP 암호
              </div>
              <div class="item-option-340">
                <button class="option-btn-s-dark">변경</button>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                 FTP 접속설정
              </div>
              <div class="item-option-340">
                <input type='radio' name='connect' value='permit' id="permit" checked/> <label for="permit" title="접속허용">접속허용</label>&emsp;
                <input type='radio' name='connect' value='nopermit' id="nopermit" /> <label for="nopermit" title="접속제한">접속제한</label>&emsp;
              </div>
              <div class="item-title">
                SSH 접속설정
              </div>
              <div class="item-option-340">
                <input type='radio' name='sconnect' value='spermit' id="spermit"/> <label for="spermit" title="접속허용">접속허용</label>&emsp;
                <input type='radio' name='sconnect' value='snopermit' id="snopermit" checked/> <label for="snopermit" title="접속제한">접속제한</label>&emsp;
              </div>
            </div>
          </div>

        </div>
      </div>

      <div class="option-grid">
        <div class="option">
          <div class="option-title">
            <h1>DB정보</h1>
            <p>DB정보를 확인 합니다.</p>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                DB 명
              </div>
              <div class="item-option-340">
                <p class="font-basic">khm10090</p>
              </div>
              <div class="item-title">
                DB 정보
              </div>
              <div class="item-option-340">
                <p class="font-delete">MySQL 8.0</p>
              </div>
            </div>
          </div>
          <div class="option-setting">
            <div class="option-items">
              <div class="item-title">
                DB 아이디
              </div>
              <div class="item-option-340">
                <p class="font-delete">khm10090</p>
              </div>
              <div class="item-title">
                DB 암호
              </div>
              <div class="item-option-340">
                <button class="option-btn-s-dark">변경</button>
              </div>
            </div>
          </div>
        </div>
      </div>




      <div class="page-btn">
        <button class="btn-save" title="저장하기">저장하기</button>
        <router-link to="/admin/dashboard/terms"><button class="btn-next" title="다음으로">다음으로</button></router-link>
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


