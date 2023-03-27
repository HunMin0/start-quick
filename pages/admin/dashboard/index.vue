<template>
  <div>

    <div class="option-grid-two">
      <div class="option">
        <div class="option-title">
          <h1>상태현황</h1>
          <p>운영중인 홈페이지의 현재상태를 안내합니다.</p>
        </div>
        <div class="option-status">
          <div class="status-item">
            <h1>서비스상태</h1>
            <a href="#" class="color-activation" title="준비중">준비중</a>
          </div>
          <div class="status-item">
            <h1>메뉴설정</h1>
            <a href="#" class="color-inactivec" title="미등록">미등록</a>
          </div>
          <div class="status-item">
            <h1>디자인적용</h1>
            <a href="#" class="color-basic" title="제작중">제작중</a>
          </div>
          <div class="status-item">
            <h1>호스팅만료일</h1>
            <a href="#" class="color-emphasis" title="2025-03-10">2025-03-10</a>
          </div>
          <div class="status-item">
            <h1>파비콘설정</h1>
            <a href="#" class="color-inactivec" title="미등록">미등록</a>
          </div>
          <div class="status-item">
            <h1>카카오톡 썸네일</h1>
            <a href="#" class="color-inactivec" title="미등록">미등록</a>
          </div>
          <div class="status-item">
            <h1>도메인상태</h1>
            <a href="#" class="color-inactivec" title="미등록">미등록</a>
          </div>
          <div class="status-item">
            <h1>SSL상태</h1>
            <a href="#" class="color-inactivec" title="미등록">미등록</a>
          </div>
        </div>
      </div>
      <div class="option">
        <div class="option-title">
          <h1>관리메모</h1>
          <p>운영관련 메모를 남겨주세요.</p>
        </div>
        <div class="option-memo">
          <textarea name="work-records" id="work-records" cols="30" rows="10" placeholder="공유하실 업무 관련 내용을 등록해주세요."></textarea>
          <div class="btn-area">
            <p>최종수정일 : &nbsp;<span>2023-03-30</span></p>
            <input type="submit" value="등록" class="option-btn">
          </div>
        </div>
      </div>
    </div>

    <div class="option-grid-two">
      <div class="option">
        <div class="option-between">
          <h1>공지사항</h1>
          <p><a href="#" title="더보기">더보기</a></p>
        </div>
        <div class="option-board">
          <ul class="board-list">
            <li>
              <label for="board-check">
                <input type="checkbox" id="board-check" name="board-notice">
                <p>01.</p>
              </label>
              <div class="board-subject">
                <p><a href="#">퀵스타트 홈페이지를 찾아주셔서 감사합니다.</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
            <li>
              <label for="board-check2">
                <input type="checkbox" id="board-check2" name="board-notice">
                <p>02.</p>
              </label>
              <div class="board-subject">
                <p><a href="#">퀵스타트 홈페이지를 찾아주셔서 감사합니다.</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
            <li>
              <label for="board-check3">
                <input type="checkbox" id="board-check3" name="board-notice">
                <p>03.</p>
              </label>
              <div class="board-subject">
                <p><a href="#">퀵스타트 홈페이지를 찾아주셔서 감사합니다.</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
          </ul>
          <div class="btn-area">
            <div class="check-delete">
              <input type="checkbox" value='selectall' name="board-notice" id="all-check">
              <label for="all-check">전체선택</label>
            </div>
            <div class="btn-group">
              <input type="submit" value="삭제" class="option-btn-outline">
              <input type="submit" value="등록" class="option-btn">
            </div>
          </div>
        </div>
      </div>

      <div class="option">
        <div class="option-between">
          <h1>문의내역</h1>
          <p><a href="#" title="더보기">더보기</a></p>
        </div>
        <div class="option-board">
          <ul class="board-list">
            <li>
              <label for="board-check4">
                <input type="checkbox" id="board-check4" name="board-notice">
                <div class="bd-noclear">미답변</div>
              </label>
              <div class="board-subject">
                <p><a href="#">템플릿 모달 업로드 시 어떻게 처리하나요?</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
            <li>
              <label for="board-check5">
                <input type="checkbox" id="board-check5" name="board-notice">
                <div class="bd-clear">답변</div>
              </label>
              <div class="board-subject">
                <p><a href="#">템플릿 모달 업로드 시 어떻게 처리하나요?</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
            <li>
              <label for="board-check6">
                <input type="checkbox" id="board-check6" name="board-notice">
                <div class="bd-noclear">미답변</div>
              </label>
              <div class="board-subject">
                <p><a href="#">템플릿 모달 업로드 시 어떻게 처리하나요?</a></p>
                <p>2023-03-30</p>
              </div>
            </li>
          </ul>
          <div class="btn-area">
            <div class="check-delete">
              <input type="checkbox" value='selectall' name="board-notice" id="all-check2">
              <label for="all-check2">전체선택</label>
            </div>
            <div class="btn-group">
              <input type="submit" value="삭제" class="option-btn-outline">
              <input type="submit" value="등록" class="option-btn">
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="option-grid-two">
      <div class="option">
        <div class="option-between">
          <h1>접속자통계</h1>
          <p>2023.03.31(금) 12: 22 &emsp;
            <select name="date" class="date-selectbox">
              <option value="today" class="date-option">오늘</option>
              <option value="yesterday" class="date-option">어제</option>
              <option value="weekly" class="date-option">주간</option>
              <option value="monthly" class="date-option">월간</option>
              <option value="year" class="date-option">년간</option>
            </select>
          </p>
        </div>
        <div class="option-container">

        </div>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: "dashboard",
  layout: "admin",
  data: () => ({

  }),

}
</script>


