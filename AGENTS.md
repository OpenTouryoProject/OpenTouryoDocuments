# プロジェクト ポリシー
主に当該リポジトリの内容を、

https://github.com/OpenTouryoProject/OpenTouryo/wiki

に移行する作業を行う。

## コンテンツ作成

- 日本語版コンテンツの拡張子は、*.ja.*とする。

-作業範囲「XXXXX」（例：UserGuide）で、

  - マークダウン配置位置「..\OpenTouryo.wiki\XXXXX」
  - イメージ配置位置「..\OpenTouryo.wiki\images\XXXXX\YYYY\」
    - YYYYはマークダウンを識別できる文字列
    - 短いセクション名を使用する（UserGuide_IndexならIndex）。

## GitHubの操作
gh で認証し、gitで操作する。

## 更新操作はpushしない

**新規作成時を除き、更新操作において成果物の検収は人が行う。** エージェントは作業結果をワーキング ツリーに残すところまでを担当し、Git 操作は人が手動で行う。

従って、更新操作において指示がない限り次を実行して検収前・未レビューの変更を確定・送信しない。

- `git commit` / `push`

また、人の作業状態や未保存の作業を壊すので、以下の操作は行わない。

- `git checkout` / `switch` / `branch` / `reset` / `restore` / `stash`

修正作業が完了したら**何を変更したかを報告するに留める**。コミットの要否とタイミングは人が判断する。

<!--
  補足（執筆者向け）:
  インストラクションは「文脈」であって強制力を持たない。上記は遵守されやすい書き方に
  しているが、確実に阻止したい場合は仕組み側で塞ぐ必要がある。
    - Claude Code : PreToolUse フックで Bash(git commit:*) 等を deny する
    - 各プロダクト: 同等の機構があればそれを使う
  必要になったら install.ps1 に設定の配布を追加することを検討する。
-->

