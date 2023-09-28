---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: OSSに初めてPRを出してみた話
mdc: true
---

# OSSに初めてPRを出してみた話

テックソリューション室 SI事業部 フロントエンド開発G<br>
福西俊介

<style>
  h1 {
    font-size: 20px;
  }
</style>
---
transition: fade-out
hideInToc: true
level: 1
---

# 目次

<Toc />
<br>
<br>

---
layout: default
---

# はじめに

<div class="outline">
  <p class="outline-text">
    つい先日、初めてOSSにPRを上げてみました。<br>
    特にこのプロジェクトに貢献したいというものはなく、ただOSS活動の一歩目を踏み出してみようという思いでした。
    もともとOSS活動は上級者だけができるのだという考えを持っていましたが、初心者にもできることがあると知り、始めてみました。今回はPRを上げるまでの流れであったり、感想などを話せればと思います。
  </p>
  <a href="https://github.com/iiitl/Wanderlusters/issues/3" target="_blank" rel="noopener noreferrer">対応したIssue</a>
</div>


<style>
.outline {
  margin-top: 40px;
  color: white;
  font-size: 21px;
  outline-style: none;
}
.outline-text {
  line-height: 2.5rem;
}
.links {
  margin-left: 20px;
}
</style>
---
transition: fade-out

level: 1
---

# OSSとは

<section>
  <div class="explanation">
    Open Source Softwareの略で、ソースコードが公開されていて、誰でも自由に無償で改変、再配布ができるソフトウェアのことです。<br>
    一般的に会社で扱うプロジェクトのソースコードは社外に漏れないように非公開であることが多いです。
    <br><br>
  </div>
  <div class="examples">
    <span>
      例：<br>
    </span>
    <div>
      ・WordPress<br>
      ・Git<br>
      ・VSCode<br>
      ・Java<br>
      ・Python<br>
      <span class="etc">など...</span>
    </div>
  </div>
</section>


<style>
  section {
    margin-top: 40px;
  }
  .explanation {
    margin-top: 40px;
  }
  .examples {
    display: flex;
    margin-top: 40px;
    gap: 20px;
  }
  .etc {
    padding-left: 20px;
  }
</style>
---
---

# 対応するIssueの見つけ方

<div class="image-container">
  <div class="column1">
    <p>対応するIssueの見つけ方はいくつかあります。その中でも特に初心者向けの易しいIssueを見つける方法を2つ紹介します。</p>
    <p>
      - 
      <a href="http://github-help-wanted.com/" target="_blank" rel="noopener noreferrer">
        Github Help Wanted
      </a>
    </p>
    <p>
      Github Help Wantedでは言語と目的に関するラベルを用いて自分の求めているIssueを検索できる。
    </p>
    <p class="good-first-issue">
      - 
      <a href="https://goodfirstissue.dev/" target="_blank" rel="noopener noreferrer">
        good first issue
      </a>
    </p>
    <p>
      good first issueのラベルがついたIssueがまとまっているサイトで、言語を選んで目的のIssueを検索できる。
    </p>
  </div>
  <div class="images">
    <img src="/public/github-help-wanted.jpg" width="300" height="auto" />
    <img src="/public/good-first-issue.jpg" width="300" height="auto" />
  </div>
</div>

<style>
.image-container {
  margin-top: 24px;
}
.good-first-issue {
  padding-top: 8px;
}
.images {
  display: flex;
  justify-content: center;
  gap: 20px 40px;
}
</style>
---
---

# 見つける際のポイント

<div class="image-container">
  <div class="column1">
    <p>- 該当のIssueに対してコメント数が少ない</p>
    <p>コメント数が多いIssueは、対応する前に仕様や方針について確認することが多くなり取り掛かりに時間がかかる。</p>
    <p>- easyのラベルがある</p>
    <p>Issueのラベルにgood first issueだけでなく、easyがあると初めてOSS活動する人にとって、より取り掛かりやすいものになる。</p>
    <p>- Issueが作成された日付が浅い</p>
    <p>古くからあるIssueは長い間解決されてこなかった可能性があり、初めてのOSS活動には向かない。</p>
  </div>
</div>

<style>
.image-container {
  display: flex;
  align-items: center;
  margin-top: 40px;
}
.column1 {
  margin-right: 20px;
}
.column2 {
  width: 50%;
  height: auto;
}
img {
  width: 100%;
  height: 100%;
}
table {
  margin-bottom: 20px
}
</style>

---

# Issue対応の進め方

<div class="image-container">
  初心者向けのIssueを管理者が登録している場合の対応の流れを下に記述します。
  <div class="column1">
    <p>- 修正するプロジェクトをForkする。</p>
    <p>- 修正するIssueの対応の前にプロジェクトの管理者に対応する旨を伝える。</p>
    <p>- ローカルで挙動を確認した後、新しくブランチを切って修正対応をする。</p>
    <p>- 対応した内容をpushし、PRを上げる。</p>
    <p>- PRにはIssue番号や対応前後の挙動がわかる画像や動画を添付する。</p>
    <p>- PRがマージされたらIssueをクローズして終了。</p>
  </div>
</div>

<style>
.image-container {
  margin-top: 40px;
}
.column1 {
  margin-top: 32px;
}
</style>

---
class: px-20
---

# 修正対応してみた感想

<div class="image-container">
  最初は何年も経験があるエンジニアじゃないとOSS活動ができないと思っていましたが、初心者向けのIssueなど対応しやすいものがあると知って行動できました。OSS活動におけるルールや普段自分で開発する中ではない手順を経験できたのが良かったです。今後はもう少し難しい内容のIssue対応もできればと思います。
</div>

<style>
.image-container {
  margin-top: 60px;
}
</style>
---
preload: false
---


# 参考

<div class="wrapper">
https://blog.zaim.co.jp/n/n9af19d9fef28<br><br>
https://tech.gunosy.io/entry/oss_first_contribution<br><br>
<span>https://untitledreport.com/%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AEoss%E3%82%B3%E3%83%B3%E3%83%88%E3%83%AA%E3%83%93%E3%83%A5%E3%83%BC%E3%83%88%E3%81%BE%E3%81%A7%E3%81%AE%E9%81%93%E7%AD%8B/</span>
</div>

<style>
  .wrapper {
    margin-top: 40px;
  }
  span {
    overflow-wrap: break-word;
  }
</style>
---

<h2>
  ご静聴ありがとうございました!
</h2>

<style>
  div {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>