# 研究室Webサイト サンプル

GitHub Pages、Jekyll、[Academic Pages](https://github.com/academicpages/academicpages.github.io)を使った研究室Webサイトのサンプルです。

掲載されている大学名、研究室名、人物、研究業績、授業情報、住所、メールアドレス、外部リンクはすべて架空のサンプルです。公開前に実際の情報へ差し替えてください。

## ページ構成

- ホーム：`_pages/about.md`
- 研究内容：`_pages/research.md`
- 教員紹介：`_pages/faculty.md`
- メンバー：`_pages/members.md`、`_data/members.yml`
- 研究業績：`_pages/publications.html`、`_publications/`
- 担当科目：`_pages/teaching.html`、`_teaching/`
- アクセス：`_pages/access.md`
- メニュー：`_data/navigation.yml`
- サイト全体の設定：`_config.yml`
- 追加スタイル：`assets/css/main.scss`

## 最初に変更する項目

`_config.yml` の次の値を実際の情報へ変更します。

```yaml
title: "研究室名"
name: "研究室名"
description: "サイトの説明"
url: "https://organization-name.github.io"
repository: "organization-name/organization-name.github.io"
```

同じファイルの `author` 以下に、研究室名、所属、所在地、連絡先を設定してください。

## Teachingの更新

科目は `_teaching/` に1科目1ファイルで登録します。

```yaml
---
title: "科目名"
collection: teaching
status: current       # current または past
academic_year: 2026
term: "前期"
schedule: "月曜2限"
schedule_order: 1
date: 2026-04-01
permalink: /teaching/course-slug/
summary: "一覧に表示する概要"
---
```

担当終了時は `status: current` を `status: past` に変更します。

## ローカル確認

RubyとBundlerを用意した後、初回だけ依存関係をインストールします。

```bash
bundle install
```

ローカルサーバーを起動します。

```bash
bundle exec jekyll serve
```

ブラウザで `http://localhost:4000/` を開きます。`_config.yml` を変更した場合はサーバーを再起動してください。

## GitHub Pagesでの公開

1. GitHub Organizationに `organization-name.github.io` という公開リポジトリを作成します。
2. このサイトのファイルをリポジトリへpushします。
3. `Settings` → `Pages` → `Build and deployment` を開きます。
4. `Deploy from a branch`、デフォルトブランチ、`/(root)` を選択します。
5. `Actions`画面でビルド成功を確認します。

## 公開前チェック

- サンプルの名称、文章、住所、メールアドレスをすべて置換したか
- 学生本人から氏名・写真・研究テーマ掲載の同意を得たか
- 大学名・ロゴ・外部サービス利用に関する規程を確認したか
- PDFや画像に非公開情報や位置情報が残っていないか
- スマートフォンとPCの両方で表示を確認したか
- `bundle exec jekyll build --strict_front_matter` が成功するか

## ライセンス

テーマ部分はAcademic PagesおよびMinimal Mistakesのライセンスに従います。`LICENSE`を保持してください。サイト固有の文章・画像については、公開時に研究室の方針を明記してください。
