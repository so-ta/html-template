# scss + js をwebpackでbundleして作るウェブページの最小構成
まずは `npm install` をしてください。

`npm start` で開発環境向けビルド  
`npm run start:prod` で本番環境向けにビルド  
  
サンプルのサーバーを立てての確認は、 `docker-compsoe up` で行えます。  
  
```
ディレクトリ構成
docker Dockerファイル等
node_modules
public sassやjsをbundleしたファイルが置かれます。
src sassやjsをbundleする前のファイルが置かれます。
views htmlが置かれます。 error/404.htmlは404時に表示されます
```

## ライブラリ等
webpack, webpack-cli：  
  JavaScriptなどの複数のモジュールをひとつにまとめるツールです。    
　複数のjsファイルをひとつのjsファイルにまとめたり、複数のsassファイルをひとつのsassファイルにしたりできます。

@babel/core、@babel/preset-env、babel-loader：  
　ES6記法を以前のバージョンに対応するものへコンパイルします。  
　`babel.config.js` に対応するブラウザは記載しています。
  
cross-env：  
　npmスクリプト実行時に任意の環境変数を設定できます。

css-loader, sass-loader, node-sass：  
　webpack上でscssをコンパイルする  

postcss-loader, cssnano：  
　cssのコンパイル結果のベンダープレフィックス付与や、  
　minifyを行います。

extract-text-webpack-plugin：  
　webpack上でビルドしたcssを保存します。  
