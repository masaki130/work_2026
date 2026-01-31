# 自己教師あり学習モデルを使用した音声感情強度推定

# 説明
* [Huggingface](https://huggingface.co/)に公開されているSSLで音声特徴量を抽出
* 上記を入力として，感情カテゴリはロジスティック回帰，感情強度はリッジ回帰を用いて学習
* データセットは[OGVC](https://research.nii.ac.jp/src/OGVC.html)を使用

# 導入方法
```
$ git clone git@github.com:masaki130/work_2026.git
```

## 必要なソフトウェア
* Python
  * テスト済み：3.11

## テスト環境
* Ubntu：24.04

## ライセンス
* [こちら]()を参照
