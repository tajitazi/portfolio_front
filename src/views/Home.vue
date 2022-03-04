<template>
  <div class="home">
    <main>
      <!-- メインビジュアル -->
      <div class="py-4">
        <div class="container">
          <!-- カルーセル外枠 -->
          <div id="main_visual" class="carousel slide" data-bs-ride="carousel">
            <!-- インジケーター -->
            <ol class="carousel-indicators">
              <li data-bs-target="#main_visual" data-bs-slide-to="0" class="active"></li>
              <li data-bs-target="#main_visual" data-bs-slide-to="1"></li>
              <li data-bs-target="#main_visual" data-bs-slide-to="2"></li>
            </ol>
            <!-- / インジケーター -->
            <!-- カルーセル内枠 -->
            <div class="carousel-inner">
              <!-- スライド01 -->
              <div class="carousel-item active">
                <img class="img-fluid" src="../assets/slide_01.jpg" alt="1枚目画像">
                <div class="carousel-caption d-none d-md-block">
                  <h2>ポートフォリオサイト作りました</h2>
                  <p>説明欄</p>
                </div>
              </div>
              <!-- / スライド01 -->
              <!-- スライド02 -->
              <div class="carousel-item">
                <img class="img-fluid" src="../assets/slide_02.jpg" alt="2枚目画像">
                <div class="carousel-caption d-none d-md-block">
                  <h2>ポートフォリオサイト作りました</h2>
                  <p>説明欄</p>
                </div>
              </div>
              <!-- / スライド02 -->
              <!-- スライド03 -->
              <div class="carousel-item">
                <img class="img-fluid" src="../assets/slide_03.jpg" alt="3枚目画像">
                <div class="carousel-caption d-none d-md-block">
                  <h2>ポートフォリオサイト作りました</h2>
                  <p>説明欄</p>
                </div>
              </div>
              <!-- / スライド03 -->
            </div>
            <!-- / カルーセル内側 -->
            <!-- コントローラー -->
            <a class="carousel-control-prev" href="#main_visual" role="button" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true"></span>
              <span class="visually-hidden">前に戻る</span>
            </a>
            <a class="carousel-control-next" href="#main_visual" role="button" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true"></span>
              <span class="visually-hidden">次に進む</span>
            </a>
          <!-- / コントローラー -->
          </div>
          <!-- / カルーセル -->
        </div>
      </div>
      <!-- / メインビジュアル -->
      <!-- コンテンツ01 -->
      <div class="py-4">
      {{responseApi}}
      </div>
      <!-- /コンテンツ01 -->
      <div class="py-4 bg-light">
        <section id="topPage">
          <div class="container">
            <!-- 上段 -->
            <div class="row mb-4">
              <div class="col-md-12 mb-3">
                <h3 class="mb-3">ポートフォリオタイトル</h3>
                <p>このポートフォリオでは、私のプロフィール・スキル・業務経歴についてまとめさせていただきました。</p>
              </div>
            </div>
            <!-- /上段 -->
            <!-- 下段 -->
            <div class="row">
            <div class="col-md-4">
              <div class="card mb-3">
                <a href="/about">
                  <img src="../assets/profile_top.png" alt="Profile" class="img-fluid">
                </a>
                <div class="card-body d-flex justify-content-between">
                  <h4 class="card-title">Profile</h4>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="card mb-3">
                <a href="/skill">
                  <img src="../assets/skill_top.png" alt="Skill" class="img-fluid">
                </a>
                <div class="card-body d-flex justify-content-between">
                  <h4 class="card-title">Skill</h4>
                </div>
              </div>
            </div>
            <div class="col-md-4">
              <div class="card mb-3">
                <a href="/work">
                  <img src="../assets/work_top.png" alt="Work" class="img-fluid">
                </a>
                <div class="card-body d-flex justify-content-between">
                  <h4 class="card-title">Work</h4>
                </div>
              </div>
            </div>
          </div>
          <!-- /下段 -->
        </div>
      </section>
    </div>
    </main>   
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data(){
    return{
      responseApi: ""
    }
  },
  mounted(){
    axios
      .get('http://127.0.0.1:8000/api/history_list')
      .then(response => (this.responseApi = response))
  }
}
</script>
  