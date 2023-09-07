Linuxサーバー上でalgiaを使ってNostrにポストするWebhookを作るツールです。
Pythonを使っています。

Linuxサーバー上にNostrにポストを投稿するためのWebhookを作ります。

前提としてalgia (https://github.com/mattn/algia)が動作している事が必要です。
Linuxサーバー上で動いているalgiaを起動させる仕組みになっています。
リポジトリのconfig.jsonはこのプロジェクト用ではなく、algiaのおすすめのコンフィグです。PrivateKeyを書き換えて使ってください。

PostToNostr.pyを実行すると、「http:<yourdomain>:5000/webhook」で起動するWebhookになります。

Webhookに対してPostアクションで
{ “id-key” : ”test-key”,”text” : “POSTしたい文字列" }
というJSONを
"Content-Type: application/json" とContent-Typeを指定してHTTPでPOSTすればNostrに投稿されます。

実際に使う際はPostToNostr.pyの「/webhook」を好きなアクセスURLに、ポートを変える際は「port:5000」を好きなポートに、アクセスキーを変えるには「"test-key”」を変えてください。