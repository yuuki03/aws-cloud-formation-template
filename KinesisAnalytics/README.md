# kinesis-firehose.yaml

## 概要
- KinesisFirehoseをストリーミングソースとして可動するKinesisAnalytics
- CWLのログを扱っているKinesisFirehoseをデータ元としている想定
    - そのためLambdaを利用している
- アプリケーションのSQLは含めていないので作成後に自分で書く必要がある
- KinesisFirehoseは出来ている前提

## 作成される資産
- IAM Role
- Kinesis Analytics Application

## 入力値
- KinesisAnalyticsAplicationName
    - 作成するアプリケーションの名前
- KinesisAnalyticsAplicationDescription
    - アプリケーションの説明
- InputSorceKinesisFirehoseARN
    - 入力元のKinesisFirehoseのarn
- InputProcessingLambdaFunctionARN
    - 入力データを整形するLambdaのarn

