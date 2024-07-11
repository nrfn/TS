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



## 変数宣言の型注釈
TypeScriptでは変数宣言時に型を指定することができる。

```
変数名: 型 = 値;
string型    : 文字列
number型    : 数値
boolean型   : true, false
any型       : なんでも入る
null型      : null
undefined型 : undefined
ユニオン型    : 型 | 型 → 複数型を指定できる
```



## 変数宣言の型推論
変数宣言時の型注釈は必須ではない。\
TypeScriptは変数宣言時に代入された値からその型を推論する。\
コンパイラが型を自動で判別する機能を型推論という。
```
// 代入された値からstring型と推論
let name = "nrfn";

// string型の変数に数値を代入しているためエラー
name = 3;
```



##  配列
型の後ろに[]を書く。
```
let animals: string[] = ["bird", "cat", "dog"];
animals = ["monkey", "panda"];

// string型の配列に数値の配列を代入しているためエラー
animals = [4, 5];

// string型の配列に文字列を代入しているためエラー
animals = "gorilla"; 
```



## オブジェクト型
オブジェクトはプロパティの集合体。\
プロパティはキーと値のペア。\
オブジェクトの型注釈は、プロパティ形式で記述。
```
let me: { name: string; age: number } = { name: "nrfn", age: 27 };

me = { name: "shh", numberOfLegs: 32 };

// プロパティageがないためエラー
me = { name: "nrfn" };

// string型に数値を代入しているためエラー
me = { name: 2, age: 13 };
```