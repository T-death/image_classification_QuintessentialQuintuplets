# 五等分の花嫁の顔画像分類  

ディレクトリの構造
```
.
├── custom_dataset
│   ├── images
│   │   ├── train # 訓練データセット(画像)
│   │   │   ├── 0001.png
│   │   │   ├── 0002.png
│   │   │   └── ...
│   │   └── valid # 検証データセット(画像)
│   │       ├── 0004.png
│   │       ├── 0008.png
│   │       └── ...
│   └── labels
│       ├── train # 訓練データセット(ラベル)
│       │   ├── 0001.txt
│       │   ├── 0002.txt
│       │   └── ...
│       └── valid # 検証データセット(ラベル)
│           ├── 0004.txt
│           ├── 0008.txt
│           └── ...
├── data
│   └── csv
│       └── image_url.csv # 元画像サイズの画像URLが記述されたcsvファイル
└── notebook
    ├── 00_scraping_imageURL.ipynb # 画像URLをスクレイピング
    ├── 01_scraping_image.ipynb # 取得した画像URLから画像をダウンロード
    ├── 03_preprocess.ipynb # YOLOv7による学習に必要な前処理
    ├── 04_exec_yolov7.ipynb # YOLOv7による学習
    └── 05_test.ipynb # テストデータに対する実行
```

必要な準備
* labelImgのインストール  
    + [こちら](https://github.com/heartexlabs/labelImg)に従って環境を整える
* YOLOv7のインストール  
    + [こちら](https://github.com/WongKinYiu/yolov7)からインストール(=gitクローン)
* インストールしたライブラリはいずれもルートディレクトリに置いておくと良いかも