# timer.js
GameTest のライブラリです。
このライブラリは`setInterval`や`setTimeout`をGameTestに追加します。

## 導入方法
1. [Releases](https://github.com/Lapis256/timer.js/releases)からダウンロードし`scripts`フォルダ内に入れてください
2. `manifest.json`で指定したエントリーファイルの先頭で`timer.js`をインポートしてください

## サンプル
```js
import "./timer.js";

setInterval(() => {
    console.warn("20tick 毎に実行されるテキスト");
}, 20);

setTimeout(() => {
    console.warn("200tick 後に表示されるテキスト");
}, 200);
```

## 使い方
### setInterval
指定した関数を指定したtick毎に実行します。
#### 構文
```js
const id = setInterval(func, delay[, param1, param2, ...]);
```
#### 引数
- `func`: `delay`が経過するたびに実行される関数です。
- `delay`: 関数の実行まで待つ時間を tick で指定します。
- `param1, ..., paramN`: 省略可能です。`func`を実行する際に渡される引数です。
#### 返り値
インターバルを識別するためのIDを返します。

***

### clearInterval
[setInterval](#setinterval) で設定したインターバルをキャンセルします。
#### 構文
```js
clearInterval(id);
```
#### 引数
- `id`: キャンセルするインターバルのidです。

***

### setTimeout
指定した関数を指定した時間が経過した後に実行します。
#### 構文
```js
const id = setTimeout(func, delay[, param1, param2, ...]);
```
#### 引数
- `func`: `delay`が経過した後に実行される関数です。
- `delay`: 関数の実行まで待つ時間を tick で指定します。
- `param1, ..., paramN`: 省略可能です。`func`を実行する際に渡される引数です。
#### 返り値
タイムアウトを識別するためのIDを返します。

***

### clearTimeout
[setTimeout](#settimeout) で設定したタイムアウトをキャンセルします。
#### 構文
```js
clearTimeout(id);
```
#### 引数
- `id`: キャンセルするタイムアウトのidです。

