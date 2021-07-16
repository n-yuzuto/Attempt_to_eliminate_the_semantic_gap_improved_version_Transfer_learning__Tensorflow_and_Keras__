# Attempt_to_eliminate_the_semantic_gap_improved_version_Transfer_learning__Tensorflow_and_Keras__
kaggleのデータ「Dogs vs. Cats」から犬と猫のカラー画像をCNNで学習し、犬と猫の画像を分類させました。  
# Attempt_to_eliminate_the_semantic_gap__Tensorflow_and_Keras__
こちらの改良版になります。kerasのVGG16モデルを使って、転移学習を行いました。VGG16は、16層（プーリング層とFlatten層はカウントしない）の
畳み込みニューラルネットワークで、ImageNetという大規模な画像データセットの学習を進めることで、1000カテゴリのマルチクラス分類を行ったものです。
詳しくは読みやすいブログがありましたので、こちらをご覧ください。  
[VGG16について](https://newtechnologylifestyle.net/vgg16networkvisual/)

ただし、最終出力は1000カテゴリの分類なので、2値分類には使えないので、出力側のFC層は使用せずに、直前の畳み込みブロックまでを使いました。
最後のFC層を独自のものに置き換えて、最終出力を1個のニューロンのミニして2値分類を行いました。

【考察】  
テストデータの精度は95%となりました。自作のCNNのモデルは73%だったので、その差は歴然でした。


***
.ipynbファイルが開かれない時は、こちらのリンクにURLを貼ってご覧になってください。  
[nbviewer](https://nbviewer.jupyter.org/)
