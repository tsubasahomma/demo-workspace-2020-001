# デモ用ワークスペース

このワークスペースは [Liferayユーザー会 東京 : Liferay 7.2でのサイト構築ベストプラクティス・ハンズオン] で使用したLiferayワークスペースです。ほぼデフォルト構成ですが、次の追加があります：

1. [Freemarkerのリソース変更チェックを無効化するOSGi設定ファイル]
2. [Clayベースのデモ用テーマ]

このワークスペースの作成手順を[Qiitaの記事]にしたので、興味のある方は併せて参照してみてください。

# ツールとバージョンの前提

**OS**

macOS Catalina 10.15.3

**Java**

```bash
$ java -version
java version "1.8.0_231"
Java(TM) SE Runtime Environment (build 1.8.0_231-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.231-b11, mixed mode)
```

**Node.js**

```bash
$ node -v
v10.17.0
```

**[Blade]**

```bash
$ blade version
blade version 3.9.0.202001232132
```

# 使用方法
```bash
$ git clone https://github.com/tsubasahomma/demo-workspace-2020-001.git
$ cd demo-workspace-2020-001
$ blade server init # ワークスペース内にバンドルを展開（バンドルをダウンロードするため、時間がかかる場合があります）
$ blade server run # バンドルをフォアグラウンドで起動（バックグラウンドで起動する場合: blade server start）
$ cd themes/my-liferay-theme # デモ用テーマへ移動
$ npm install # 依存関係をインストール（警告が出ますが動作には問題はありません）
$ gulp init # テーマのデプロイ先を指定
$ gulp init deploy # ワークスペースに展開されたバンドルへデプロイ
```
<!--  -->
[Liferayユーザー会 東京 : Liferay 7.2でのサイト構築ベストプラクティス・ハンズオン]:https://liferay.doorkeeper.jp/events/102935
[Qiitaの記事]:https://qiita.com/TsubasaHomma/items/4c037024040e0bb636b4
[Clayベースのデモ用テーマ]:https://github.com/tsubasahomma/demo-workspace-2020-001/tree/master/themes/my-liferay-theme
[Freemarkerのリソース変更チェックを無効化するOSGi設定ファイル]:https://github.com/tsubasahomma/demo-workspace-2020-001/blob/master/configs/local/osgi/configs/com.liferay.portal.template.freemarker.configuration.FreeMarkerEngineConfiguration.config

[Blade]:https://portal.liferay.dev/docs/7-2/reference/-/knowledge_base/r/installing-blade-cli
