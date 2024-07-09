# TS
TypeScriptgit 学習用のリポジトリです。

## 環境構築
- nvmをインストール
```
# installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

- nvmを利用してNode.jsをインストール
```
# download and install Node.js (you may need to restart the terminal)
nvm install 20
```

- TypeScriptをグローバルインストール
```
npm install -g typescript
```

- tsconfig.jsonを作成
```
tsc --init
```

## 実行とコンパイル
.tsファイルをコンソール上で実行する場合
```
node FileName.ts
```

.jsファイルにコンパイルして実行する場合
```
# .tsから.jsにコンパイル
tsc FileName.ts

# .jsファイルの実行
node FileName.js
```