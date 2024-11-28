# python

■python インストール
≪手順≫
https://www.python.jp/install/windows/index.html

≪インストール媒体≫
https://pythonlinks.python.jp/
https://www.python.org/ftp/python/3.12.3/python-3.12.3-amd64.exe

①インストール
・上記をダウンロードしてインストーラを起動
インストール時に"Add Python 3.x to PATH" をチェックするのを忘れないように。

②インストール確認
・インストール完了後、コマンドプロンプトを起動して、「python」を入力しエラーとならないことを確認。

③PowerShellでスクリプトの実行を許可
・PowerShellにて以下のコマンドを実行（１回のみ）
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force


■仮想環境の構築
https://www.python.jp/install/windows/venv.html
①仮想環境の作成
python -m venv .venv
（バージョン指定は、py -3.7 -m venv py37env）

②仮想環境への切り替え
.venv\Scripts\activate.bat or Activate.ps1

③仮想環境の終了
deactivate

■vscodeによる開発環境構築
https://www.python.jp/python_vscode/windows/index.html

追加拡張機能は以下
Python Extension for Visual Studio Code

memo
Shift＋Enterで対象行のみ実行

■コマンド備忘録
≪パッケージインストール≫
・デフォルトバージョンへのインストール
python -m pip install パッケージ名
pip install pandas

・バージョンを指定してのインストール
py -3.7 -m pip install パッケージ名

≪パッケージアンインストール≫
python -m pip uninstall パッケージ名

■便利パッケージ
①Excelを使用（VBAと違い開いていないファイルに対して実行可能）
openpyxl
※Office 2010以降のxlsxなどの拡張子のみ対応。xlsなどは正常に動かない可能性あり

■文法チート
①パッケージの使い方
import pandas as pd
df = pd.DataFrame({"a":[1,2,3], "b":[11,12,13]}, index =["aa", "bb", "ccc"])

②Excelワークブックを作成
from openpyxl import Workbook
wb = Workbook()
ws = wb.active
ws.title = 'test'
wb.sava("test.xlsx")


■旧エクセルを開くためには以下をインストールする必要あり
pip install xlrd
