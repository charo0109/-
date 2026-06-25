# 左右反転画像 生成プログラム flip.py
## 1. 概要
引数で指定した画像の左右反転画像を作成する python3 で動作するプログラムです。
## 2. ソースコード
```python3
# このプログラムは python3 用です。
# あらかじめ pip insta pillow で pillow をインストールしておきます。
from PIL import Image
import sys

# コマンドライン引数から入力画像と出力画像のファイルを取得
input_image = sys.argv[1]
output_image = sys.argv[2]

# 画像の読み込み
img = Image.open(input_image)

# 画像の左右反転
img_flip = img.transpose(Image.FLIP_LEFT_RIGHT)

# 画像の保存
img_flip.save(output_image)
```
## 3. 使い方
### 3.1. 実行例
- コマンドインフォーマット
```python3
python3 flip.py<input_image_path><output_image_path>
```
- 利用例
```python3
python3 flip.py inout.jpg output.jpg
```
### 3.2. 出力結果
-以下のように入力画像の左右反転画が出力されます。
| 入力画像(input.jpg) | 出力画像(output.jpg) |
| ![入力画像](C:\Users\k_himeno\Downloads\CL-12_圧縮解凍後index.htmlを開く\CL-12_圧縮解凍後index.htmlを開く\利用素材\input.jpg) | ![出力画像](C:\Users\k_himeno\Downloads\CL-12_圧縮解凍後index.htmlを開く\CL-12_圧縮解凍後index.htmlを開く\利用素材\output.jpg) |
以上
