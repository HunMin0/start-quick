<template>
  <v-container class="mypageBg" fluid>
    <v-row class="justify-center content-center">
      <div class="vCardLoginBg">
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
              <p class="firstTextTitle">비밀번호를 잊으셨나요? <img src="/images/padlock.png" alt="padlock" /></p>
              <p class="lastTextTitle">가입시 등록하신 휴대폰 번호를 입력해주세요 인증 후 비밀번호 재설정이 가능합니다.</p>
            </div>
            <v-card-text class="pa-0">
                <v-card elevation="0" class="pa-0 ma-0 d-flex">
                <v-text-field prepend-inner-icon="mdi-phone" class="inpBottom vinpuT"
                              label="핸드폰번호" persistent-hint hint="'-' 없이 번호만 입력 해주세요." outlined />&emsp;
                <v-btn large elevation="0" color="primary" height="56">핸드폰인증</v-btn>
                </v-card>
            </v-card-text>
            <v-card-actions class="pa-0">
              <v-btn :disabled="disabledSave" @click="save" color="primary" block x-large>비밀번호 찾기</v-btn>
            </v-card-actions>
            <div class="settingBox2">
              <router-link to="/member/login"><v-icon color="primary" class="iconMa3">mdi-chevron-left</v-icon>로그인 돌아가기</router-link>
            </div>
          </v-card>
        </v-col>
      </div>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "password",
  auth: 'guest',
  layout: 'login',
  data: () => ({
    form: {},
    errors: {},
  }),
  methods: {

  }
}
</script>
<style scoped>
  ::v-deep .vinpuT .v-label {color: #969696;}
  ::v-deep .vinpuT .v-input__slot {padding: 0 18px!important;}
  ::v-deep .v-text-field fieldset, .v-text-field .v-input__control, .v-text-field .v-input__slot {border: 1px solid #d4d3d5;}
  ::v-deep .fText .v-label {font-size: 14px;}
  .loginLogo {margin-bottom: 2rem;display: flex;-webkit-box-align: center;align-items: center;-webkit-box-pack: center;justify-content: center;}
  .loginLogo img {height: 58px;}
  .firstTextTitle {margin: 0px 0px 0.375rem;font-size: 1.25rem;line-height: 1.334;color: rgba(58, 53, 65, 0.87);font-weight: 600;}
  .lastTextTitle {font-weight: 400; font-size: 0.875rem; line-height: 1.5; letter-spacing: 0.15px; color: rgba(58, 53, 65, 0.68);}
  .loginTextB {margin-bottom: 1.5rem;}
  .inpBottom {margin-bottom: 16px;}
  .settingBox {font-size: 14px; margin-bottom: 28px; display: flex; -webkit-box-align: center; align-items: center; flex-wrap: wrap; -webkit-box-pack: justify; justify-content: space-between;}
  .settingBox2 {margin: 28px 0; text-align: center; font-size: 14px; color: rgba(58, 53, 65, 0.68);}
  .snsform {flex-shrink: 0; display: flex; white-space: nowrap; text-align: center; border: 0px;  margin-bottom: 14px;}
  .snsform span {display: inline-block; padding-left: calc(0.3rem); padding-right: calc(0.3rem);}
  .snsform::before {position: relative; width: 100%; border-top: thin solid rgba(58, 53, 65, 0.12); top: 50%; content: ""; transform: translateY(50%);}
  .snsform::after {position: relative;  width: 100%; border-top: thin solid rgba(58, 53, 65, 0.12); top: 50%; content: ""; transform: translateY(50%);}
  .snsSetting {display: flex; -webkit-box-align: center; align-items: center; -webkit-box-pack: center; justify-content: center;}
  .firstTextTitle img {height: 28px;}

@media (min-width: 600px){
  .vCardLoginBg {
      width: 448px;
  }

}
</style>
