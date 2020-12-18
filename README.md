# gltf ファイルを圧縮する方法

# 参考にした記事

（１）gltf pipeline 公式サイト
https://github.com/CesiumGS/gltf-pipeline
（２）誰かのサイト
https://codelabo.com/posts/20200830135244

# やり方

任意のディレクトリに、gltf ファイルをおいておく。
（今回は Donloads > archive > .gltf）です。

（１）まずは node.js をインストールする。
ここから LTS をインストールしておく
https://nodejs.org/ja/

（２）gitf pipeline のコマンドを打つ

```bash
npm install -g gltf-pipeline
```

エラーができたらこれを読んでください。
https://github.com/i-am-ethan/npmError

（２）gltf の階層までいってコマンドを打つ（自分の場合）

```bash
#現在地を確認する
ls
cd Downloads
cd archive
#archiveのなかにgltfがある。たどり着いたら以下のコマンド

#Converting a glTF to Draco glTF
gltf-pipeline -i model.gltf -o modelDraco.gltf -d
```

（３）けっかはっぴょ〜〜う
どれくらい差がでたのか？
圧縮前：5M
圧縮後：3.4M

そこそこでた？
よかったらやってみてください。
