# Megalo Image Generator Pro v1.43 初心者チュートリアル

## ダウンロードとインストール

Releasesから `Megalo_Pro_v1.43_GitHub_Free_protected_20260724.zip` をダウンロードします。GitHubが自動生成するソースコードZIPはインストール用ではありません。

ZIPを展開し、`chrome://extensions`でデベロッパーモードを有効にして `ja_JP/extension` を読み込みます。

## Cloud Runバックエンドの更新

v1.43には新しいGeminiモデルが含まれるため、v1.42から更新する場合は付属のv1.43スクリプトでCloud Runバックエンドを再デプロイしてください。

## v1.43モデル

- 既定の画像: `gemini-3.1-flash-image`
- 高品質画像: `gemini-3-pro-image`
- 低コスト1K画像: `gemini-3.1-flash-lite-image`
- 既定のテキスト: `gemini-3.6-flash`
- 軽量テキスト代替: `gemini-3.5-flash-lite`

終了したPreviewモデルは削除され、古い選択は自動移行されます。Flash Lite Imageは1K専用です。

## 古い設定の復元

古いプリセット、キャラクターファイル、フォルダーバックアップ、暗号化バックアップを復元しても、現在のBackend URLスロット1～10は上書きされません。
