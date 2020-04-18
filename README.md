# 大阪府市町村の陽性者数　可視化

# ファイル構成
- index.html：JavaScriptもCSSも書いている
- yousei.csv：市町村の陽性者。あえて３列目は空白として、陽性者数に応じた色名を後で保有
- osakapref.json：市町村の境界path（緯度経度）とyousei.csvとのキーをindexに保持
- cityname.csv：市町村名表示用。市町村名と表示位置の緯度経度（要調整）
- Web.config: AzureのWebAppsに挙げる時のコンフィグ

# プログラム
- yousei.csvを読み込み、陽性者数を５段階に応じて、３列目に色名を保持させる
- D3を用い、svgで大阪府市町村の境界を描画
- pathのデータは「osakapref.json」から取得する
- 市町村の色は３列目に保持させている色名で塗る
- cityname.csvを読み込んで緯度経度に市町村名を描画


フォルダのファイルをローカルに置き、Servedをインストールして読み込ませると動く
