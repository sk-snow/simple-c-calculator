# C言語で作成したシンプルな電卓

このプロジェクトは、C言語で作成されたコマンドライン上の簡易電卓です。

## ファイル構成

- `main.c`：エントリーポイント。`Calculator()` 関数を呼び出すだけの構成。
- `calculator.c`：電卓のロジックとユーザー入力処理を担当。
- `calculator.h`：`Calculator()` の関数プロトタイプを定義。
---

## コンパイル方法

以下のコマンドでコンパイルできます：

```bash
gcc main.c calculator.c -o simple-c-calculator
```
---

## 注意事項 (使用環境)

このプログラムは`scanf_s`を使用しており、
**Visual Studio 2022などのWindows環境**でのビルドを想定しています。
GCCやClangを使う他の環境では```scanf_s```はサポートされていないため、
置き換える必要があります

---

## 他の環境でビルドするには？

Visual studio以外の環境(GCCやClangなど)では、
`scanf_s` を標準の `scanf` に置き換えてください。

例：
```c
//	数値入力の場合 (double型など)
scanf_s("%lf", num);	//	Visual Studio
↓
scanf("%lf", num);		//	標準C

//	文字の読み取りなど、バッファ操作が必要な場合
sscanf_s(buffer, "%c", symbol, 1);
↓
sscanf(buffer, "%c", symbol);

```

---

## 実行方法

```
./simple-c-calculator
```
---

## 主な機能

- 四則演算(+, -, *, /)に対応
- 無効な入力へのエラーハンドリング
- y/nによる継続確認付きループ処理
---

## 補足

- 本プロジェクトは学習目的で作成されたものです。
- 今後のアップデート予定はありません。
---

[英語版READMEはこちら](README.md)