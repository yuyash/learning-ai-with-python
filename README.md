# Learning AI with Python

このリポジトリは Python と Jupyter Notebooks を使って AI を学ぶ過程で、試したコードや学んだ内容を記録するための個人的なノートです。

このリポジトリは自分自身の学習記録として作成しており、他の誰かにそのまま利用してもらうことは意図していません。内容の正確性や再現性は保証せず、学習の進行に応じて構成やコードを変更します。

## 利用する場合のセットアップ

Python と依存ライブラリは [uv](https://docs.astral.sh/uv/) で管理しています。

### 1. uv をインストールする

macOS では Homebrew を使ってインストールできます。

```shell
brew install uv
```

その他の環境やインストール方法については [uv の公式ドキュメント](https://docs.astral.sh/uv/getting-started/installation/) を参照してください。

### 2. リポジトリを取得する

```shell
git clone https://github.com/yuyash/learning-ai.git
cd learning-ai
```

### 3. Python 環境を構築する

次のコマンドで、指定された Python と依存ライブラリをインストールします。仮想環境はプロジェクト内の `.venv` に作成されます。

```shell
uv sync
```

### 4. JupyterLab を起動する

```shell
uv run jupyter lab
```

表示された URL をブラウザで開いて使用します。終了するときは、コマンドを実行したターミナルで `Ctrl+C` を押します。
Visual Studio Code を利用する場合はノートブックファイルを開いて、`uv sync` によって作成されたカーネルを選択して実行します。

## 補助コマンド

コードのチェックには Ruff と ty を使用します。

```shell
uv run ruff check .
uv run ruff format --check .
uv run ty check .
```

Ruff で修正可能な問題を直し、コードを整形します。

```shell
uv run ruff check --fix .
uv run ruff format .
```
