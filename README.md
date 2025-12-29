# Px2XY

Px2XY は画像中の粒子の重心を検出し、参照点（RefPoint）を使ってピクセル座標を実世界座標に変換するための GUI ツールです。

## 特徴
- 画像から重心（centroids）を抽出
- 参照点を追加・編集してアフィン / 類似変換を推定
- 転置表示の参照テーブルと即時プレビュー

## 必要環境
- Python 3.10+（環境に合わせて調整してください）
- 依存パッケージは `requirements.txt` を参照

## インストール（開発用）
```powershell
cd C:\Python\Px2XY
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## 実行方法
GUI を起動するには:
```powershell
py Main.py
```

## 使い方（簡易）
- `Open Image` で画像を開く
- `Add Ref` で参照点追加モードにして画像上で参照点をクリック
- 左の参照テーブルで Obs.X/Obs.Y/Obs.Z を編集して再計算

## 開発・貢献
- バグ報告・機能要望は GitHub Issues へお願いします
- プルリクエスト歓迎

## ライセンス
このリポジトリは `LICENSE` の定める条件に従います。

## 引用
リリース済みの DOI がある場合はここに追記してください（Zenodo 経由で DOI を発行することを推奨）。

---
（この README は自動生成されました。必要に応じて追記・修正してください）
# Px2XY — Centroid Finder

Px2XY は画像をポスタリゼーション（色クラスタリング）して領域ごとの重心を検出・表示する GUI ツールです。
主に画像解析、顕微鏡画像の特徴点抽出、参照点設定・エクスポートに使えます。

## 主な機能
- 画像の読み込みと表示（多数のフォーマットをサポート）
- ポスタリゼーションによる領域クラスタリングと重心検出
- PyQt5 ベースの GUI（参照点の追加・編集、重心の選択、CSV 形式でのエクスポート等）
- 自動/手動更新モード、軽負荷モード対応

## 必要条件
- Python 3.8 以上
- 以下の主要パッケージ（詳細は `requirements.txt` を参照）
  - numpy
  - opencv-python
  - PyQt5

注: 実行環境や用途に応じて追加パッケージが必要になる場合があります。

## インストール
仮想環境を作成し、依存パッケージをインストールする例（PowerShell）:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt
```

## 実行方法（簡易）
GUI を起動するにはリポジトリルートで:

```powershell
python Main.py
```

Main.py をコマンドライン引数で画像パスを与えて起動できる場合は、次のように実行します:

```powershell
python Main.py path\to\image.jpg
```

## 使い方（概要）
- PosterLevel, Min Area, Trim を調整して興味ある領域の抽出精度を調整します。
- 参照点（Ref）を追加して座標を固定・保存できます。
- 重心はテーブルから選択、エクスポート可能です。

詳しい操作手順や図は `paper.md`（JOSS 投稿用）およびドキュメントで説明します。

## ライセンス
このプロジェクトは `LICENSE` に記載のライセンス下で公開されています（例: MIT）。

## 引用
このソフトウェアを使った研究を報告する場合は `CITATION.cff` を確認してください。

## 貢献
PR や Issue を歓迎します。コードスタイルやテストを整備した上でプルリクエストを送ってください。

## 作者
あなたの名前（適宜更新してください）
