# 麻雀牌の物体検出

## テスト

1. darknetをインストール
```
git clone https://github.com/AlexeyAB/darknet.git
cd darknet
```

2. make
```
vi Makefile # GPU=1にする
make
```

3. [cfg/datasets.txt](cfg/datasets.txt)の中身を適切に書き換える
4. GoogleDriveから学習済みファイルをダウンロード(https://gist.github.com/iamtekeste/3cdfd0366ebfd2c0d805)
```
gdrive_download 1DGptwQKU_v0CkjZcDnvaDI42w5HI00B3 ../cfg/yolo-obj.weight
```

5. 実行
```
./darknet detector test ../cfg/datasets.txt ../cfg/yolo-obj.cfg ../cfg/yolo-obj.weights ../data/sample.jpg
```