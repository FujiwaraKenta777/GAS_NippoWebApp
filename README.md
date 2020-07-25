# 概要

弊社規定の「終業後三時間以内に業務報告（日報）を送付しないと賞与減額」の罰則を受けないために、LINEBOTで送付有無を確認するメッセージを送る。

# 導入

![QR](https://user-images.githubusercontent.com/53109614/88427077-39651f00-ce2d-11ea-9b0e-4fc3cbe78385.png)

# 仕様

 * 18:30~23:30 まで日報を送ったか確認メッセージを送ってくれる。

 * 「送った」、「今日は休み」と返事したときは労いの言葉をかけて、その日はもう確認メッセージは送らない。
 
 * 「これから」と返事したときは催促のメッセージを送り、再度30分後に確認のメッセージを送る。

 * なにも返事をしなかったときに、すごく催促する

# TODO

* メッセージ以外の返事

# 開発環境メモ

直接LineBotとやりとりしているプロジェクト。

ライブラリとしてNIPPO(GAS_NippoLibrary)プロジェクトを導入している。

![readme_1](https://user-images.githubusercontent.com/53109614/88421400-7af0cc80-ce23-11ea-91dc-29adc5e763fa.png)

30分間隔でトリガーを設定している。

![Trigger](https://user-images.githubusercontent.com/53109614/88425750-e1c5b400-ce2a-11ea-96b2-40b6c7a48de2.png)
