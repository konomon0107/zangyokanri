# zangyokanri

# 概要
## アプリの概要
残業管理を行うためのアプリ。
デバイスに依存しない(クロスプラットフォーム)Webアプリ。
ローカルアプリでは共有しにくいデータをWeb上で共有する。

## 概要図
![Alt text](system.jpg)

# 機能一覧
・ログイン機能
・ユーザー管理
・残業申請登録
・残業申請承認
・勤怠確認

# 画面一覧
・トップ画面
・ログイン画面
・残業履歴集計画面
・残業申請登録画面
・残業申請承認画面
・勤怠確認画面

# 遷移図
![Alt text](flow.jpg)

# テーブル定義
|ユーザーテーブル|      |                  |
|--------|------|------------------|
|カラム名    |データ型  |説明                |
|ユーザーID  |STRING|個人が決めたID          |
|ユーザ名    |STRING|氏名                |
|パスワード   |STRING|                  |
|ユーザータイプ |STRING|一般<br>承認者<br>勤怠確認者|
|部署ID    |STRING|

|残業データテーブル|       |            |
|---------|-------|------------|
|カラム名     |データ型   |説明          |
|データID    |INTEGER|            |
|ユーザーID   |STRING |            |
|登録日時     |DATE   |            |
|残業時間     |FLOAT  |30min = 0.5h|
|残業理由     |STRING |            |
|勤務種別     |STRING |            |
|承認フラグ    |BOOL   |            |
|勤怠管理フラグ  |BOOL   |            |
|承認者      |STRING |            |
|承認日時     |DATE   |
# 技術スタック
## インフラ
・GCE
## フロント
・react
## バックエンド
django
## ソース管理
・github
## データベース
・mysql