# kinesis-firehose.yaml

## 概要
- 所定のS3バケットにデータを転送するKinesisFirehoseを作成するCloudFormationTemplateのサンプル

## 作成される資産
- IAM Role
- Kinesis Firehose　DeliveryStream

## 入力値
- KinesisFirehoseDeliveryStreamName
    * KinesisFirehoseの名前
- KinesisFirehoseDeliveryStreamType
    * DirectPut | KinesisStreamAsSource
- DestinationS3BucketArn
    * 出力先S3バケットのarn
- KinesisFirehoseBufferingIntervalInSeconds
    * Bufferする時間最短60sec-最大900sec
- KinesisFirehoseBufferingSizeInMBs
    * 最低１MB〜
- KinesisFirehoseOutputErrorLogGroupName
    * firehoseがエラーを出したときに出力するCloudWatchLogsのGroup名
- KinesisFirehoseOutputErrorLogStreamName
    * Stream名
- KinesisFirehoseCompressionFormat
    *　圧縮形式
        - `UNCOMPRESSED` が基本
- KinesisFIrehoseToS3Prefix
    * S3格納時のPREFIXを指定する。最後に `/` が必要
- KinesisFirehoseIAMRoleName
    * firehoseが使用するIAM Role名