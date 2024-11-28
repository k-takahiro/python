# python

■python インストール<br/>
≪手順≫
https://www.python.jp/install/windows/index.html

≪インストール媒体≫<br/>
https://pythonlinks.python.jp/
https://www.python.org/ftp/python/3.12.3/python-3.12.3-amd64.exe<br/>

①インストール<br/>
・上記をダウンロードしてインストーラを起動<br/>
インストール時に"Add Python 3.x to PATH" をチェックするのを忘れないように。<br/>

②インストール確認<br/>
・インストール完了後、コマンドプロンプトを起動して、「python」を入力しエラーとならないことを確認。<br/>

③PowerShellでスクリプトの実行を許可<br/>
・PowerShellにて以下のコマンドを実行（１回のみ）<br/>
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force<br/>


■仮想環境の構築<br/>
https://www.python.jp/install/windows/venv.html<br/>
①仮想環境の作成<br/>
python -m venv .venv<br/>
（バージョン指定は、py -3.7 -m venv py37env）<br/>

②仮想環境への切り替え<br/>
.venv\Scripts\activate.bat or Activate.ps1<br/>

③仮想環境の終了<br/>
deactivate<br/>

■vscodeによる開発環境構築<br/>
https://www.python.jp/python_vscode/windows/index.html<br/>

追加拡張機能は以下<br/>
Python Extension for Visual Studio Code<br/>

memo<br/>
Shift＋Enterで対象行のみ実行<br/>

■コマンド備忘録<br/>
≪パッケージインストール≫<br/>
・デフォルトバージョンへのインストール<br/>
python -m pip install パッケージ名<br/>
pip install pandas<br/>

・バージョンを指定してのインストール<br/>
py -3.7 -m pip install パッケージ名<br/>

≪パッケージアンインストール≫<br/>
python -m pip uninstall パッケージ名<br/>

■便利パッケージ<br/>
①Excelを使用（VBAと違い開いていないファイルに対して実行可能）<br/>
openpyxl<br/>
※Office 2010以降のxlsxなどの拡張子のみ対応。xlsなどは正常に動かない可能性あり<br/>

■文法チート<br/>
①パッケージの使い方<br/>
import pandas as pd<br/>
df = pd.DataFrame({"a":[1,2,3], "b":[11,12,13]}, index =["aa", "bb", "ccc"])<br/>

②Excelワークブックを作成<br/>
from openpyxl import Workbook<br/>
wb = Workbook()<br/>
ws = wb.active<br/>
ws.title = 'test'<br/>
wb.sava("test.xlsx")<br/>


■旧エクセルを開くためには以下をインストールする必要あり<br/>
pip install xlrd<br/>
