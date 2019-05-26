# 初期設定

## 目次


## GitHubに登録する
やっておいてね！！！  
https://github.com/

<br>

## gitをインストールする（MacOS）

### Homebrew をインストール
https://brew.sh/index_ja  

このスクリプトをターミナルに貼り付けて実行する
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

### gitをインストール
```
brew install git
```

### インストールが成功したことを確認
```
git help
# => ヘルプが表示されたら成功。
```

<br>

## gitをインストールする（Windows）

### ダウンロード
このページを開き、セットアップを実行する。  
https://git-scm.com/download/win

### インストール
ここを参照してください。  
https://eng-entrance.com/git-install


### インストールが成功したことを確認
Git Bashをひらいて、以下のコマンドを入力する。
```
git help
# => ヘルプが表示されたら成功。
```

<br>

## SSH公開鍵をGitHubに登録する（MacOS）
### SSH鍵の作成

以下のコマンドを実行。  
メールアドレスはGitHubに登録したものを使う。  
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

SSH Keysの保存先を聞かれるが、特に気にしなければそのままEnter  
```
Enter file in which to save the key 
(/Users/you/.ssh/id_rsa): [Press enter]
```

パスフレーズの入力を求められるので、入力する。  
初めてこの鍵を使ってアクセスするときに入力を求められる。  
```
Enter passphrase (empty for no passphrase): [Type a passphrase]
# Enter same passphrase again: [Type passphrase again]
```

これで作成は完了です。

<br>

### SSH公開鍵をGitHubに登録する

GitHubにログインし、 https://github.com/settings/keys を開く。  
<br>
![](https://i.imgur.com/1U99e8i.png)  

公開鍵をクリップボードにコピーする
```
pbcopy < ~/.ssh/id_rsa.pub
```

<br>

New SSH Keyをクリックし、Keyの欄に先程コピーした公開鍵をペーストする。  
Title を入力して "Add SSH key" をする。
<br>
![](https://i.imgur.com/SoL8HTd.png)

これで完了。

<br>

## SSH公開鍵をGitHubに登録する（Windows）

WindowsでのSSHはハマりポイントが多く、本題の操作に影響がある可能性があるので今回はHTTPSで行います。🙇‍♂️  

HTTPSでのクローン方法は別途説明します。

