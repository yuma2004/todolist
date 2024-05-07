# GitとGitHubの使い方

## Gitのインストール

1. **Windows**:
   - [Git for Windows](https://gitforwindows.org/)にアクセスしてインストーラーをダウンロードし、指示に従ってインストールします。

2. **macOS**:
   - Homebrewを使用してインストール: ターミナルを開いて、以下のコマンドを実行します。
     ```
     brew install git
     ```

3. **Linux**:
   - Debian/Ubuntu系のディストリビューションで以下のコマンドを使用します。
     ```
     sudo apt-get update
     sudo apt-get install git
     ```
   - FedoraなどのRed Hat系ディストリビューションでは以下のコマンドを使用します。
     ```
     sudo dnf install git
     ```

## GitHubアカウントの設定

1. [GitHub](https://github.com/)にアクセスし、「Sign up」ボタンからアカウントを作成します。
2. 必要な情報を入力して登録を進め、メールアドレスの確認を行います。

## Gitの基本的な設定

1. ユーザー名とメールアドレスの設定:
   - Gitでコミットする際に使用するユーザー名とメールアドレスを設定します。
     ```
     git config --global user.name "your_username"
     git config --global user.email "your_email@example.com"
     ```

2. 新しいリポジトリの作成:
   - GitHubで「New repository」ボタンをクリックし、リポジトリ名と説明を入力します。
   - リポジトリをプライベートまたはパブリックに設定できます。

## 基本的なGitコマンド

1. **git clone**:
   - GitHub上のリポジトリをローカルにコピーします。
     ```
     git clone https://github.com/username/repository.git
     ```

2. **git add**:
   - 変更したファイルをステージングエリアに追加します。
     ```
     git add .
     ```

3. **git commit**:
   - ステージングエリアのファイルの変更を記録します。
     ```
     git commit -m "Add your message"
     ```

4. **git push**:
   - ローカルの変更をGitHubにプッシュします。
     ```
     git push origin main
     ```

5. **git pull**:
   - GitHubから最新の変更をローカルリポジトリに取り込みます。
     ```
     git pull origin main
     ```

このドキュメントは、GitとGitHubの基本的な使用方法を新しいユーザーに紹介するためのものです。続けて他の技術スタックについても同様の解説を作成する場合は、その旨をお知らせください。
