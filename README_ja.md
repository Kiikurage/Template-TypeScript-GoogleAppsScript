# Template-TypeScript-GoogleAppsScript

GoogleAppsScriptをローカルで、TypeScriptで開発するためのテンプレート

## 初期設定

1. GoogleAppsへファイルをアップロードするためのツール `node-google-apps-script` をインストールする

    ```bash
    $ yarn global add node-google-apps-script
    ```

2. ファイルをプロジェクトへアップロードするために、GoogleDriveAPIを使えるようにする

    1. GoogleAPIコンソールへ行って、新しくプロジェクトを作成するか、既存のプロジェクトを1つ選ぶ
    2. プロジェクトのAPI設定画面へ行き、 Drive API を有効化する
    3. 認証情報を作成し、認証情報のJSONをダウンロードする
    4. JSONを登録する

        ```bash
        $ gapps auth <authorized_json_file>
        ```

3. アップロード先のGoogleAppsScriptプロジェクトを紐付ける

    1. GoogleAppsScriptプロジェクトを新規作成するか既存プロジェクトを開く
    2. FileIDを取得する。FileIDはURL中に `https://script.google.com/d/<FileID>` の形で入っている.
    3. FileIDを登録する

        ```bash
        $ gapps init <FileID>
        ```

以降は、 `gapps upload` コマンドで `/src` 以下のファイルが自動的にアップロードされる。
