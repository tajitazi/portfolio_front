<template>

<nav class="navbar navbar-expand-md navbar-dark bg-dark sticky-top">
  <!-- サブコンポーネント -->
  <div class="container">
    <a class="navbar-brand" href="index.html">ポートフォリオ</a>
    <!-- 切り替えボタン -->
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbar-content" aria-controls="navbar-content" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <!-- ナビゲーション -->
    <div class="collapse navbar-collapse" id="navbar-content">
      <!-- ナビゲーションメニュー -->
      <!-- 左側メニュー：トップページの各コンテンツへのリンク -->
      <ul class="navbar-nav me-auto">
        <li class="nav-item active">
          <a class="nav-link" href="/">Profile<span class="visually-hidden">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">Skill</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Work</a>
        </li>
      </ul>
      <!-- 右側メニュー：お問い合わせページへのリンク -->
      <ul class="navbar-nav">
        <li class="nav-item">
          <a href="contact.html" class="nav-link btn btn-info text-dark">Contact</a>
        </li>
      </ul>
      <!-- /ナビゲーションメニュー -->
    </div>
  </div>
  <!-- /サブコンポーネント -->
</nav>

</template>