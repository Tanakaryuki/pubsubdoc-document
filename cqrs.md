# CQRS ハンズオン環境構築資料

## 目次

1. 概要
2. バージョン一覧
3. 環境構築手順
   - 3.1. プロジェクトのセットアップ
   - 3.2. IntelliJ IDEA のインストール
4. Java の環境構築
5. 動作確認

## 1. 概要

この資料では、GMO インターネットの成瀬さんによる CQRS ハンズオンの開発環境を構築するための手順を説明します。当日までに以下の手順に従って環境を整えてください。  
今回の CQRS ハンズオンでは、Java を使用して開発します。
![rns](https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/3827c4de-1044-428e-b8de-a8fc83f84b8c)

## 2. バージョン一覧

動作確認済みのバージョンは以下の通りです  
動作確認はしていませんが windows や Linux でも動作すると思います(多分!!)

- **OS**： macOS Sonoma14.5
- **プログラミング言語**：Java 21.0.3 Amazon Corretto
- **IDE**：IntelliJ IDEA 2024.1.4
- **バージョン管理ツール**：git 2.39.3
- **コンテナツール**：Docker 26.1.4

## 3. 環境構築手順

### 3.1. プロジェクトのセットアップ

1. Git リポジトリのクローン作成：
   ```bash
   git clone git@github.com:nrslib/pubsubdoc.git
   ```

### 3.2. IntelliJ IDEA のインストール

1. [IntelliJ IDEA 公式サイト](https://www.jetbrains.com/ja-jp/idea/download)からインストーラーをダウンロードし、インストールする
   <img width="794" alt="install_done" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/7f45d0f8-7fbb-4fae-8d49-9ec9f8cf83d3">

2. Open から先ほどクローンしたプロジェクトを開く(開くと場合によってはロードやビルドしてくれる可能性あり)
   <img width="1392" alt="open_done" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/f1316feb-ff34-4ea1-93e3-4e059708cbee">

## 4. Java の環境構築

1. SDK の設定
   File -> Project Structure を開く
   <img width="1510" alt="setting_open_done" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/c176d540-4b9e-49f6-96f7-a39dbbd9f22f">
2. Project -> SDK -> Download SDK... をクリック
   <img width="1512" alt="select_SDK" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/c5d36527-004d-4516-819a-f434fd10601b">
3. SDK のバージョンを選択  
   Amazon Corretto 21.0.3 aarch64 を選択 (x86_64 の場合、無印を選択)  
   ダウンロードボタンを押す
   <img width="1512" alt="download_SDK" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/090e3641-4c57-4b54-b389-196980e554e7">
4. Language Level を SDK Default に設定  
    OK ボタンを押す
   <img width="1512" alt="change_language_level" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/f6de6ac1-aa9a-44f1-96de-3a32533bad90">
5. Gradle JVM を設定  
   IntelliJ IDEA -> setting
   <img width="1512" alt="change_setting" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/f1dd0430-87c4-4060-802c-8f55bead4f88">
6. Gradle を検索  
   Gradle JVM を Project SDK corretto-21 に設定(元から設定されている場合も)
   <img width="1512" alt="search_gradle" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/f1b41ac6-d27e-4943-a3d4-b550ba147556">

## 5. 動作確認

1. build.gradle.kts を開き、右上の再生ボタン(Run)をクリック
   <img width="1512" alt="run" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/9da59ae8-f210-412c-be90-389a53a100b3">
   起動後
   <img width="1512" alt="runed" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/8c391a73-5fcc-4fc5-83ce-0118afb16d09">
2. ブラウザで localhost:8080 にアクセスして Swagger が動作していることを確認する
   <img width="1511" alt="check" src="https://github.com/Tanakaryuki/pubsubdoc-document/assets/46374705/4af7a286-a5f8-458f-805a-169b58712660">

### 以上で環境構築は完了です!! CQRS ハンズオン当日をお楽しみに!!
