# 自己教師あり学習モデルを使用した音声感情強度推定

## 説明
* [Huggingface](https://huggingface.co/)に公開されているSSLで音声特徴量を抽出
* 上記を入力として，感情カテゴリはロジスティック回帰，感情強度はリッジ回帰を用いて学習
* データセットは[OGVC](https://research.nii.ac.jp/src/OGVC.html)を使用

## 導入
```
$ conda create -n ser python=3.11 -y
$ conda activate ser
$ git clone git@github.com:masaki130/work_2026.git
$ cd work_2026
$ pip install torch transformers librosa soundfile tqdm
```

## 実行環境
* Ubntu：24.04
* Python：3.11

## ライセンス
* [こちら１](https://huggingface.co/imprt/izanami-wav2vec2-large/blob/main/LICENSE.md)を参照
* [こちら２](https://huggingface.co/audeering/wav2vec2-large-robust-12-ft-emotion-msp-dim)を参照
