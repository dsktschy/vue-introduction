<template>
  <div class="page">
    <div class="page-inner">
      <p class="paragraph">
        お名前、メールアドレス、お問い合わせ内容を<br>ご記入の上、メールにてお送りください
      </p>
      <p class="paragraph">
        Webサイト制作に関するお問い合わせは<a href="mailto:yamada@ta.ro">こちら</a>
      </p>
      <p class="paragraph">
        Webサービス制作に関するお問い合わせは<a href="mailto:yamada@ta.ro">こちら</a>
      </p>
    </div>
  </div>
</template>

<style scoped>
.paragraph {
  line-height: 1.5;
  font-size: 10px;
  font-weight: 900;
  margin-top: 18px;
  &:first-child {
    margin-top: 0;
  }
  & >>> a {
    color: #aaa;
  }
}
</style>
