# コマンド

```bash
$ gcloud auth application-default login
$ gcloud config set project trading-daichi-ozaki213
# feastのインストール
$ pip install 'feast[gcp]'
# ボイラーテンプレート（OfflineStoreなどを定義するファイルなどが生成）の作成
$ feast init -t gcp
$ cd <Work Dir>
$ feast apply
$ feast teardown
```

- [CLIの認証手順](https://cloud.google.com/docs/authentication/provide-credentials-adc?hl=ja#local-dev)
- [GCPでの設定ロール一覧](https://docs.feast.dev/reference/providers/google-cloud-platform)

# 関連ページ

- [FeatureStoreが利用されるようになった背景とfeastの説明記事](https://qiita.com/f6wbl6/items/a07493db66512ef22234)
- [【公式ドキュメント】Overview](https://docs.feast.dev/getting-started/architecture-and-components/overview)
  - レジストリ：各種設定を保管するための要素（S3, GCS, DBなどから選択できる）
  - [Offline Stores](https://docs.feast.dev/getting-started/architecture-and-components/offline-store)
    - [feature_store.yamlの設定方法](https://docs.feast.dev/reference/offline-stores)
  - [Online Stores](https://docs.feast.dev/getting-started/architecture-and-components/online-store)
    - [Offline Sotreからのマテリアライズ](https://docs.feast.dev/getting-started/architecture-and-components/batch-materialization-engine)
    - [feature_store.yamlの設定方法](https://docs.feast.dev/reference/online-stores)
  - [feature server](https://docs.feast.dev/reference/feature-servers/python-feature-server)
  - [Push：OfflineStoreとOnlineStoreへ特徴量をリアルタイムで連携できる機能（コードサンプル）](https://docs.feast.dev/reference/data-sources/push)
- [インストール手順](https://docs.feast.dev/how-to-guides/feast-snowflake-gcp-aws/install-feast)
