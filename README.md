# care-label
画像認識による洗濯表示の識別

## Description
画像から洗濯表示を識別し、意味を表示する

>洗濯表示とは？  
衣服についたタグのマークのこと。  
洗濯や乾燥の方法、アイロンのかけ方やクリーニングの方法などが示されている。  
全41種類。世界共通。

### WEBアプリケーション
- TOP
![screencapture-care-label-herokuapp-2019-09-17-18_58_57](https://user-images.githubusercontent.com/20394831/65031999-44356480-d97d-11e9-976b-a46833b3f78b.png)

- 予測結果表示
![screencapture-care-label-herokuapp-predict-2019-09-17-19_00_41](https://user-images.githubusercontent.com/20394831/65032112-7a72e400-d97d-11e9-84e4-53c73b5a4c14.png)


## Features
- 洗濯表示の識別
- 意味出力

## Requirement
画像の水増し python 3.6~（f文字列）

WERアプリ
[requirements.txt](/requirements.txt)

## Usage
### 画像の水増し
1枚から約1500枚に水増し。明るさ、ノイズ、回転、移動（上下左右斜め）の加工を行う。

1. [cnn/train-seeds](/cnn/train-seeds/)下の該当するフォルダに画像をおく
2. [cnn/all-ver2.ipynb](/cnn/all-ver2.ipynb)を実行する  
(windowsの場合は、[cnn/all-ver2-win.ipynb](/cnn/all-ver2-win.ipynb))
3. [cnn/train](/cnn/train/)下の該当するフォルダに水増しされた画像が出力される


上記の方法は、一括で水増しする場合。
1枚1枚指定して水増しする場合は、[cnn/all-file.ipynb](/cnn/all-file.ipynb)を実行する。

### 学習
[cnn/predict.py](/cnn/predict.py)を実行する。

モデル、重み、学習履歴、学習過程の図が保存される。

### WEBアプリケーション
[app.py](/app.py)を実行する。  
localhost:5000から確認できる。  
