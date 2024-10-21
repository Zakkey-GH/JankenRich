# ①課題名
じゃんけん AI

## ②課題内容（どんな作品か）
プレイヤーのじゃんけんの手から、AIが勝てる確率の高い手を選択する。

## ③アプリのデプロイURL
デプロイしている場合はURLを記入（任意）

## ④アプリのログイン用IDまたはPassword（ある場合）
- ID: なし
- PW: なし

## ⑤工夫した点・こだわった点
- テーマをAIとし、ユーザーの手を学習するロジックをとりいれた。
- 戦績を分析できるようグラフを挿入した。が、途中で時間切れ。

## ⑥難しかった点・次回トライしたいこと（又は機能）
- AIでメジャーなプログラムであるPythonをフロント側で使用できるPyscriptを使用した。
- PyscriptとJavaScriptとの連携。
- AIモデルの実装
- 1st
  ベーシックな統計モデル（プレイヤーが一番出す手に対して、勝つ手を選択）
  ⇒グー→チョキ→パーなど統計的に分散値が小さくなるものに対しては有効なモデルではないので
  傾向を把握できるようなモデルに改編
    
    -2nd
   - RNN（Recurrent Neural Network）モデル
    -⇒時系列的にデータを学習させ特徴抽出させようと思ったが、学習スパンが長くなり、尚且つ諸所弊害を理解しないと
    　-扱いにくいモデルなので不採用。
     
    -3rd
    -LSTM（Long Short Term Memory）モデル
    -⇒学習のスパンがちょうどよく、途中の傾向変化にも対応できそうだったので実装にトライ。
　　　-結論、失敗。理由としてはPythonのWebAssemblyであるPyodideがtensorflowのようなネイティブコードを含むPythonパッケージをサポートしていないとのこと。

　　-4th
   -結局、1stのベーシックな統計モデルに収束させた。

## ⑦フリー項目（感想、シェアしたいこと等なんでも）
- [学び]
　-Pythonの勉強をしつつ、今はJavaScriptの勉強に専念がよいと判断。
　-いきなりPyscriptとJavaScriptの両方をやろうとして中途半端になった。遅れを取り戻したい。
-【シェア】　
-・PyscriptとJavaScriptの連携は難易度が爆上がり。データの受け渡しや同期でとにかく沼る。
-・Pyscriptだけの記述はカラーリングがなくわかりずらい。
-・Pythonの標準ライブラリーの実装は可能だが、難しい事をさせようとするとサポートしていない事が多々ある。
　
