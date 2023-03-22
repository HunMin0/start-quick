<template>
  <v-container class="mypageBg" fluid>
    <v-row class="justify-center content-center">
      <div class="vCardLoginBg joinMargin">
        <v-col class="pa-0">
          <v-card flat>
            <NuxtLink to="/">
              <div class="loginLogo">
                <img src="/images/logo.png" alt="logo" />
              </div>
            </NuxtLink>
          </v-card>
          <v-card flat>
            <div class="loginTextB">
              <p class="firstTextTitle">인생을 바꾸는 교육, OURLMS <img src="/images/helping-hand.png" alt="padlock" /></p>
              <p class="lastTextTitle">2022년 새로운 마음으로 OURLMS와 함께 공부해요!</p>
            </div>
            <v-form>
               <v-card-text class="pa-0">
                  <div class="snsform fontWeight-600">
                    <v-icon class="iconMa3">mdi-checkbox-marked-outline</v-icon><span>본인인증</span>
                  </div>
                  <v-card elevation="0" class="pa-0 ma-0 d-flex">
                  <v-text-field prepend-inner-icon="mdi-phone" v-model="form.phone" :error-messages="errors.phone" class="inpBottom vinpuT"
                                label="핸드폰번호" persistent-hint hint="'-' 없이 번호만 입력 해주세요." outlined />&emsp;
                  <v-btn large elevation="0" color="primary" height="56">핸드폰인증</v-btn>
                  </v-card>
              </v-card-text>

              <v-card-text class="pa-0">
                  <div class="snsform fontWeight-600">
                    <v-icon class="iconMa3">mdi-checkbox-marked-outline</v-icon><span>계정정보</span>
                  </div>

                <v-text-field v-model="form.userid" :error-messages="errors.userid" label="아이디" outlined  hide-details="auto" class="inpBottom vinpuT"/>
                <v-text-field v-model="form.password" :error-messages="errors.password" label="비밀번호" outlined class="vinpuT"
                              autocomplete="new-password" persistent-hint hint="비밀번호는 8자리이상 입력해주세요."
                              :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"  :type="show1 ? 'text' : 'password'"  @click:append="show1 = !show1"
                              />
                <v-text-field v-model="form.password_confirmation" :error-messages="errors.password_confirmation" class="vinpuT"
                              label="비밀번호 확인"  outlined autocomplete="new-password"
                              :append-icon="show2 ? 'mdi-eye' : 'mdi-eye-off'" :type="show2 ? 'text' : 'password'"  @click:append="show2 = !show2"
                              />
              </v-card-text>

              <v-card-text class="pa-0">
                <div class="snsform fontWeight-600">
                  <v-icon class="iconMa3">mdi-checkbox-marked-outline</v-icon><span>회원정보</span>
                </div>
                <v-text-field prepend-inner-icon="mdi-account" label="이름" v-model="form.name" :error-messages="errors.name" outlined hide-details="auto" class="inpBottom vinpuT"/>
                <v-text-field prepend-inner-icon="mdi-account" label="닉네임" v-model="form.name_nick" :error-messages="errors.name_nick" outlined hide-details="auto" class="inpBottom vinpuT"/>
                <v-text-field prepend-inner-icon="mdi-account" label="이메일" v-model="form.email" :error-messages="errors.email" outlined hide-details="auto" class="inpBottom vinpuT"/>

                <v-card elevation="0" class="pa-0 ma-0 d-flex">
                  <v-text-field readonly v-model="form.user_zip" :error-messages="errors.user_zip" id="user_zip" prepend-inner-icon="mdi-map-marker" class="inpBottom vinpuT" hide-details="auto" label="주소" outlined />&emsp;
                  <v-btn large elevation="0" color="primary" height="56" @click="addrSearch('user')">주소검색</v-btn>
                </v-card>
                <v-text-field class="inpBottom vinpuT" v-model="form.user_addr1" :error-messages="errors.user_addr1" id="user_addr1" label="상세주소1" hide-details="auto"  outlined />
                <v-text-field class="inpBottom vinpuT" v-model="form.user_addr2" :error-messages="errors.user_addr2" id="user_addr2" label="상세주소2" hide-details="auto"  outlined />
                <v-text-field class="inpBottom vinpuT" v-model="form.user_addr3" :error-messages="errors.user_addr3" id="user_addr3" label="기타주소(건물명)" hide-details="auto"  outlined />
              </v-card-text>

              <v-card-text class="pa-0">
                  <div class="snsform fontWeight-600">
                    <v-icon class="iconMa3">mdi-checkbox-marked-outline</v-icon><span>선택정보</span>
                  </div>
                  <v-text-field prepend-inner-icon="mdi-domain" label="회사/학교명" v-model="form.op_name" :error-messages="errors.op_name" outlined hide-details="auto" class="inpBottom vinpuT"/>
                  <v-card elevation="0" class="pa-0 ma-0 d-flex">
                    <v-text-field readonly prepend-inner-icon="mdi-map-marker" v-model="form.op_zip" :error-messages="errors.op_zip" class="inpBottom vinpuT" hide-details="auto" label="주소" outlined />&emsp;
                    <v-btn large elevation="0" color="primary" height="56" @click="addrSearch('op')">주소검색</v-btn>
                  </v-card>
                  <v-text-field hide-details="auto" v-model="form.op_addr1" id="op_addr1" :error-messages="errors.op_addr1" class="inpBottom vinpuT" label="상세주소1" outlined />
                  <v-text-field hide-details="auto" v-model="form.op_addr2" id="op_addr2" :error-messages="errors.op_addr2" class="inpBottom vinpuT" label="상세주소2" outlined />
                  <v-text-field hide-details="auto" v-model="form.op_addr3" id="op_addr3" :error-messages="errors.op_addr3" class="inpBottom vinpuT" label="기타주소(건물명)" outlined />

                  <v-text-field prepend-inner-icon="mdi-account-settings" label="직책/학과" v-model="form.op_sbj" :error-messages="errors.op_sbj" outlined hide-details="auto" class="inpBottom vinpuT"/>
                  <v-text-field prepend-inner-icon="mdi-relative-scale" hide-details="auto" v-model="form.op_num" :error-messages="errors.op_num" class="inpBottom vinpuT" label="사업자등록번호/학번" placeholder='"-"없이 숫자만 입력' outlined />
                  <v-card elevation="0" class="pa-0 ma-0 d-flex">
                  <v-file-input class="inpBottom vinpuT" v-model="form.op_filename" label="사업자등록증/학생증" persistent-hint hint="사업자등록증 및 학생증 사본을 첨부하여 주세요." outlined />&emsp;
                  </v-card>
              </v-card-text>

              <v-card-text class="pa-0">
                  <div class="snsform fontWeight-600">
                    <v-icon class="iconMa3">mdi-checkbox-marked-outline</v-icon><span>약관정보</span>
                  </div>
                  <div class="checBox">
                    <v-checkbox append-icon="mdi-magnify" label="(필수) 이용약관 동의" hide-details />
                    <v-checkbox append-icon="mdi-magnify" label="(필수) 만 14세 이상입니다" hide-details />
                    <v-checkbox append-icon="mdi-magnify" label="(필수) 개인정보 취급방침 동의" hide-details />
                    <v-checkbox label="(선택) 마케팅 정보 수신 동의" hide-details />
                  </div>
              </v-card-text>

              <v-card-actions class="pa-0 btnButton">
                <v-btn :disabled="disabledSave" @click="save" color="primary" block x-large>회원가입</v-btn>
              </v-card-actions>
              <div class="settingBox2">
                <span>이미 계정이 있으신가요?</span>&emsp;<router-link to="/auth/login">로그인하기</router-link>
              </div>
              <div class="snsform2">
                <span>or</span>
              </div>
              <div class="snsSetting">
                <v-btn icon dark><img src="/images/facebook.png" height="24"></v-btn>
                <v-btn icon dark><img src="/images/twitter.png" height="24"></v-btn>
                <v-btn icon dark><img src="/images/google.png" height="24"></v-btn>
                <v-btn icon dark><img src="/images/naver.png" height="24"></v-btn>
              </div>
            </v-form>
          </v-card>

          <div class="forwardingJoin content-center2 justify-center">
              <p class="bottom-margin-0 bottomFont"><v-icon color="#fff">mdi-account-box-outline</v-icon>&nbsp; LMS 강사 가입은 제휴문의를 통해 가입하실 수 있습니다.</p>
              <v-btn color="#066ea5" dark elevation="0"><v-icon small>mdi-lightbulb-outline</v-icon>&nbsp;제휴문의 바로가기</v-btn>
          </div>


        </v-col>
      </div>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "register",
  auth: 'guest',
  layout: 'login',
  data: () => ({
    show1: false,
    show2: false,
    password: 'Password',
    dialog: false,
    form: {
      user_zip: '',
      user_addr1: '',
      user_addr2: '',
      user_addr3: '',
      op_zip: '',
      op_addr1: '',
      op_addr2: '',
      op_addr3: '',
    },
    errors: {},
    dialogTitle: '',
    dialogContent: '',
    terms: '',
    privacy: '',
  }),
  methods: {
    async save() {
      this.loading = true;
      try {
        await this.$axios.$get('/sanctum/csrf-cookie');
        await this.$axios.$post('api/register', this.form)
        await this.$auth.loginWith('laravelSanctum', {
          data: {
            userid: this.form.userid,
            password: this.form.password
          },
        })
         this.$router.push('/')
      } catch (e) {
         if (e.response.status == '422') {
          this.errors = e.response.data.errors;
        }
        if (e.response.status != '422') {
          this.$toast.error(e.response.data.message);
        }
      }
    },
    addrSearch(target) {
      new window.daum.Postcode({ oncomplete: (data) => {
        // 팝업에서 검색결과 항목을 클릭했을때 실행할 코드를 작성하는 부분.
        // 각 주소의 노출 규칙에 따라 주소를 조합한다.
        // 내려오는 변수가 값이 없는 경우엔 공백('')값을 가지므로, 이를 참고하여 분기 한다.
        var addr = ''; // 주소 변수
        var extraAddr = ''; // 참고항목 변수
        //사용자가 선택한 주소 타입에 따라 해당 주소 값을 가져온다.
        if (data.userSelectedType === 'R') {
          // 사용자가 도로명 주소를 선택했을 경우
          addr = data.roadAddress;
        } else {
            // 사용자가 지번 주소를 선택했을 경우(J)
          addr = data.jibunAddress;
        } // 사용자가 선택한 주소가 도로명 타입일때 참고항목을 조합한다.
        if(data.userSelectedType === 'R'){
          // 법정동명이 있을 경우 추가한다. (법정리는 제외)
          // 법정동의 경우 마지막 문자가 "동/로/가"로 끝난다.
          if(data.bname !== '' && /[동|로|가]$/g.test(data.bname)){
            extraAddr += data.bname;
          } // 건물명이 있고, 공동주택일 경우 추가한다.
          if(data.buildingName !== '' && data.apartment === 'Y'){
            extraAddr += (extraAddr !== '' ? ', ' + data.buildingName : data.buildingName);
          } // 표시할 참고항목이 있을 경우, 괄호까지 추가한 최종 문자열을 만든다.
          if(extraAddr !== ''){ extraAddr = ' (' + extraAddr + ')'; }
            // 조합된 참고항목을 해당 필드에 넣는다.
            if (target == 'user') {
              this.form.user_addr3 = extraAddr;
            } else {
              this.form.op_addr3 = extraAddr;
            }
          } else {
            if (target == 'user') {
               this.form.user_addr3 = '';
            } else {
              this.form.op_addr3 = '';
            }

          } // 우편번호와 주소 정보를 해당 필드에 넣는다.
          if (target == 'user') {
            this.form.user_zip = data.zonecode;
            this.form.user_addr1 = addr;
          } else {
            this.form.op_zip = data.zonecode;
            this.form.op_addr1 = addr;
          }
          // 커서를 상세주소 필드로 이동한다.
          document.getElementById(target + '_addr2').focus();
      } }).open();
    },
  }
}
</script>

<style>
  ::v-deep .vinpuT .v-label {color: #969696;}
  ::v-deep .vinpuT .v-input__slot {padding: 0 18px!important;}
  ::v-deep .v-text-field fieldset, .v-text-field .v-input__control, .v-text-field .v-input__slot {border: 1px solid #d4d3d5;}
  ::v-deep .fText .v-label {font-size: 14px;}
  .loginLogo {margin-bottom: 2rem;display: flex;-webkit-box-align: center;align-items: center;-webkit-box-pack: center;justify-content: center;}
  .loginLogo img {height: 58px;}
  .firstTextTitle {margin-bottom: 10px!important;font-size: 1.25rem;line-height: 1.334;color: rgba(58, 53, 65, 0.87);font-weight: 600;}
  .lastTextTitle {font-weight: 400; font-size: 0.875rem; line-height: 1.5; letter-spacing: 0.15px; color: rgba(58, 53, 65, 0.68);}
  .loginTextB {margin-bottom: 2rem;}
  .inpBottom {margin-bottom: 16px!important;}
  .settingBox {font-size: 14px; margin-bottom: 28px; display: flex; -webkit-box-align: center; align-items: center; flex-wrap: wrap; -webkit-box-pack: justify; justify-content: space-between;}
  .settingBox2 {margin: 28px 0; text-align: center; font-size: 14px; color: rgba(58, 53, 65, 0.68);}
  .snsform {flex-shrink: 0; display: flex; white-space: nowrap; text-align: center; border: 0px;  margin: 14px 0;}
  .snsform span {display: inline-block; padding-left: calc(0.3rem); padding-right: calc(1rem);}
  .snsform::before {position: relative; width: 1%;top: 50%; content: ""; transform: translateY(50%);}
  .snsform::after {position: relative;  width: 100%; border-top: thin solid rgba(58, 53, 65, 0.12); top: 50%; content: ""; transform: translateY(50%);}
  .snsSetting {display: flex; -webkit-box-align: center; align-items: center; -webkit-box-pack: center; justify-content: center;}
  .firstTextTitle img {height: 28px;}
  .snsform2 {flex-shrink: 0; display: flex; white-space: nowrap; text-align: center; border: 0px;  margin-bottom: 14px;}
  .snsform2 span {display: inline-block; padding-left: calc(0.3rem); padding-right: calc(0.3rem);}
  .snsform2::before {position: relative; width: 100%; border-top: thin solid rgba(58, 53, 65, 0.12); top: 50%; content: ""; transform: translateY(50%);}
  .snsform2::after {position: relative;  width: 100%; border-top: thin solid rgba(58, 53, 65, 0.12); top: 50%; content: ""; transform: translateY(50%);}
  .btnButton {margin-top: 40px;}
  .checBox {padding-left: 3px;}
  .joinMargin {margin: 80px 0 50px;}
  .forwardingJoin {position: fixed; left: 0; right: 0; top: 0px; height: 70px; background: #1f8bca;border-bottom: 4px solid#6ab0d7;}
  .bottomFont {color: #fff; font-weight: 600; margin-right: 18px;}
@media (min-width: 600px){
  .vCardLoginBg {
      width: 448px;
  }
}
</style>
