# 自己教師あり学習モデルを使用した音声感情強度推定
[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.x-orange?logo=pytorch)](https://pytorch.org/)
[![Dataset](https://img.shields.io/badge/Dataset-OGVC-blueviolet)](https://research.nii.ac.jp/src/OGVC.html)
[![SSL](https://img.shields.io/badge/SSL-wav2vec2%20%7C%20HuBERT-success)](https://huggingface.co/facebook/wav2vec2-base)
[![OS](https://img.shields.io/badge/OS-Ubuntu_24.04-E95420?logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![Editor](https://img.shields.io/badge/Editor-VS_Code-007ACC?logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com/)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-red)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## 説明
* [Huggingface](https://huggingface.co/)に公開されているSSLで音声特徴量を抽出
* 感情カテゴリは[ロジスティック回帰](https://qiita.com/0NE_shoT_/items/b702ab482466df6e5569)，感情強度は[リッジ回帰](https://qiita.com/kotmats/items/1ccb41ca278e400b6197)を用いて学習
* データセットは[OGVC](https://research.nii.ac.jp/src/OGVC.html)を使用

## 導入
```
$ conda create -n ser python=3.11 -y
$ conda activate ser
$ git clone https://github.com/masaki130/work_2026.git
$ cd work_2026
$ pip install torch transformers librosa soundfile tqdm
```

## ファイルの説明
* izanami_ogvc_emo_int.ipynb
  * 産総研が開発した[いざなみ](https://huggingface.co/imprt/izanami-wav2vec2-large)というSSLを使用
  * 詳しくは[こちら](https://www.aist.go.jp/aist_j/press_release/pr2025/pr20250310/pr20250310.html)を参照
* wav2vec2_vad_ogvc_re.ipynb
  * [Wagner]()らが開発した感情推定器内部で使用されているSSLを使用
  * 詳しくは[こちら](https://arxiv.org/abs/2203.07378)を参照

## ライセンス
* 感情推定および感情強度推定のためのオリジナルコードにつきましては，
**BSD 3-Clause License** の下で公開されています．
  - © 2026, Masaki Mitani
  - 詳細は [LICENSE]()ファイルを参照してください．
* SSLにつきましては，Hugging Face で公開されている以下の事前学習モデルを使用しています．
  - **audeering/wav2vec2-large-robust-12-ft-emotion-msp-dim**  
    ライセンス: **CC BY-NC-SA 4.0 (Creative Commons Attribution-NonCommercial-ShareAlike 4.0)**  
    本モデルは **非商用利用のみに制限**されています。  
    詳細については、以下の公式モデルカードを参照してください。  
    https://huggingface.co/audeering/wav2vec2-large-robust-12-ft-emotion-msp-dim
  
  - **imprt/izanami-wav2vec2-large**  
    本モデルは **独自のライセンス**の下で配布されています。  
    ライセンス条件の詳細については、以下の公式ページを参照してください。  
    https://huggingface.co/imprt/izanami-wav2vec2-large

