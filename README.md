# articles-and-essays

技術記事（Zenn）と、哲学的考察・エッセイ（note）のアウトプットを統合管理するリポジトリです。

---

## 📁 ディレクトリ構成

```text
articles-and-essays/
├── articles/            # 【Zenn専用】技術記事・論文解説（GitHub pushで自動デプロイ）
├── books/               # 【Zenn専用】Zennの本
├── essays/              # 【note専用】哲学的考察・エッセイ（Zennには公開されません）
│   ├── template.md      # note向け執筆テンプレート
│   ├── drafts/          # 執筆中の下書き
│   └── published/       # note公開済みの記事
├── images/              # 記事内で使用する画像
└── ...
```

---

## ✍️ 執筆・公開フロー

### 1. 技術記事（Zenn）
Zennの公式GitHub連携を使用しています。

- **新規作成**:
  ```bash
  npx zenn new:article
  # または
  npm run new:article
  ```
- **ローカルプレビュー**:
  ```bash
  npx zenn preview
  # または
  npm run preview
  ```
- **公開**:
  `articles/*.md` の frontmatter で `published: true` に変更し、GitHubの `main` ブランチに push すると自動でZennに反映されます。

---

### 2. 哲学的考察・エッセイ（note）
note向けの思考メモ・論考・エッセイを管理します。Zennには自動同期されません。

- **新規作成**:
  [`essays/template.md`](./essays/template.md) をコピーして [`essays/drafts/`](./essays/drafts/) に新しい `.md` ファイルを作成します。
- **公開**:
  1. [`essays/drafts/`](./essays/drafts/) で執筆・推敲します。
  2. noteのエディタに本文を貼り付け、見出しや体裁を整えて公開します。
  3. 公開後は、ファイルを [`essays/published/`](./essays/published/) に移動し、メタ情報（公開日、noteのURL）を記録して保存します。