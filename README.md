# wash-mark-checker
画像認識による洗濯表示の識別

## Description
画像から洗濯表示を識別し、意味を表示する

>洗濯表示とは？  
衣服についたタグのマークのこと。  
洗濯や乾燥の方法、アイロンのかけ方やクリーニングの方法などが示されている。  
全41種類。世界共通。

- 洗濯表示をまとめて調べる  
![screencapture-wash-mark-checker-lolipop-io-2019-12-20-20_33_43](https://user-images.githubusercontent.com/20394831/71253446-45ef3980-236b-11ea-896a-d3e3052f4e51.png)

- 洗濯表示を個別に調べる
![screencapture-wash-mark-checker-lolipop-io-individual-2019-12-20-20_34_01](https://user-images.githubusercontent.com/20394831/71253445-45ef3980-236b-11ea-9452-7a586cfb24eb.png)


## Features
- 洗濯表示の識別
  - まとめて識別
  - 個別に識別
- 意味出力

## Usage
1. `wget --load-cookies /tmp/cookies.txt "https://drive.google.com/uc?export=download&confirm=$(wget --quiet --save-cookies /tmp/cookies.txt --keep-session-cookies --no-check-certificate 'https://drive.google.com/uc?export=download&id=1xYyucyZy3xew9jkdQk9NCa559Qvmnwg3' -O- | sed -rn 's/.*confirm=([0-9A-Za-z_]+).*/\1\n/p')&id=1xYyucyZy3xew9jkdQk9NCa559Qvmnwg3" -O trained_weights_final.h5 && rm -rf /tmp/cookies.txt`
2. `python app.py`
