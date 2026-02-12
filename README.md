## python_venv
python環境の導入方法をご共有します

## 導入の流れ
1. 環境を設立する場所(フォルダ)を用意する
2. ソフトウェアのインストール
3. 仮想環境の作成（venv）
4. ライブラリのインストール
5. 動作テスト

## 環境を設立する場所を良いする
Cドライブ直下にpythonフォルダを作成
\\C\python に仮想環境を作成していく
仮想環境は用途に応じて作成をすると効率的にプログラム開発が行える
例えばpythonのversionによって分ける、データ整形しか行わない環境など

## pythonのソフトウェアのインストールの実施
https://www.python.org/
ソフトウェアをインストールの実施
versionによって書き方が異なるケースがあるので注意が必要。
インストールの際は赤枠のチェック欄に2点チェックを入れる

<img width="384" height="240" alt="スクリーンショット 2026-02-12 100440" src="https://github.com/user-attachments/assets/298718df-e72b-4c12-b11a-3e24d2245989" />

## 仮想環境の設立
コマンドプロンプトを開いて
先ほど作成したpythonフォルダをカレントディレクトリにする
cd python と入力する

その後
python –m venv 環境名と入力する
今回env1という環境名にした。その部分は自由につけて問題ない

<img width="566" height="220" alt="スクリーンショット 2026-02-12 101040" src="https://github.com/user-attachments/assets/aaa78934-a144-44d7-9416-2cbe775b4592" />

pythonフォルダの中にenv1のフォルダが作成される

## python環境に入る
コマンドプロンプトを一度立ち上げ直す。
カレントディレクトリをpython/env1/Script/activate.batでpython環境に入れる

<img width="588" height="277" alt="スクリーンショット 2026-02-12 101659" src="https://github.com/user-attachments/assets/75c524d1-411d-429b-b452-b9ac4a35c27c" />


環境に入れると（環境名）今回ですと(env1)が表示される

<img width="525" height="114" alt="スクリーンショット 2026-02-12 101747" src="https://github.com/user-attachments/assets/c24c0784-f3bd-4140-be3c-4d4d5456e9b7" />


## ライブラリの導入
環境に入った状態で
pip install ライブラリ名
で基本はインストールできる

ex)pip install pandas

version指定してインストールする場合は
pip install pandas==2.3.3

アンインストールする場合は
pip uninstall ライブラリ名

アップデートする場合は
pip install ライブラリ名 -U

## ライブラリがプロキシーエラーを出力した場合の対処方法
各々の環境によってライブラリをインストール場合これらで引っかかる可能性がある
その場合は以下でいったん自身のプロキシを確認する
設定からネットワークとインターネット　→　プロキシ
にてプロキシを確認できる

<img width="592" height="543" alt="スクリーンショット 2026-02-12 102335" src="https://github.com/user-attachments/assets/7ecca862-225f-4cb1-8193-503f8493090c" />


pip構文を以下に変更して実行すると改善する
pip install ライブラリ名 --proxy http://プロキシのIPアドレス:ポート番号

## テストコードの実行
デスクトップ上にスクリプトを配置して以下を入力して実行を行う
カレントディレクトリをデスクトップにして
python ファイル名　で実行
今回は
python test.py

<img width="602" height="55" alt="スクリーンショット 2026-02-12 102905" src="https://github.com/user-attachments/assets/45eda4ce-5421-4ba0-8348-8c78fd85b38a" />







