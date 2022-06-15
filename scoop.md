# Scoopを使った環境構築

* 環境構築苦手な人向け
* Windows の面倒な環境構築をサポートします．WSL が使えるなら WSL でいいです． 
* Ubuntu の apt みたいな感じです．
* PyPy や C++のコマンドが使えるようになります．

## Scoopのインストール
インターネット環境下で以下のコマンドをPowerShellで実行する．(管理者権限いるかも？)　  
Execution Policy Change は Y + Enter
```
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
```

インストールが完了すればターミナルで  
(以下ターミナルと言えばコマンドプロンプト，PowerShellなど何でもいい)
```
scoop 
```
と打って
```
Usage: scoop <command> [<args>]

Some useful commands are:

alias       Manage scoop aliases
bucket      Manage Scoop buckets
...
```

のようにエラーが出なければOK.

## GCC (C++ コンパイラ) のインストール
ターミナルで以下を入力する．
```
scoop install gcc
```
以下が出ればOK (ちゃんとコードのコンパイルができるかも確認してね)
```
'gcc' (11.2.0) was installed successfully!
```


## PyPyのインストール
ターミナルで以下を入力する．
```
scoop install pypy3
```

以下が出ればOK(ちゃんとコードの実行ができるかも確認してね)

```
'pypy3' (7.3.9) was installed successfully!
```


もしかしたら GCC が必要かもなので，もしエラーが出たら GCC もインストールしてください．

## memo

同様に Python 等の install もできる．

## 注意
日本語ファイル名が使えないとかがあるのでそこが不便