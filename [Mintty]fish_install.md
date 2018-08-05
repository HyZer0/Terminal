# [Mintty] bash から fish へ乗り換え

## Cygwin 公式サイトからfishパッケージのダウンロード、インストール
1. [cygwin](https://www.cygwin.com/)をダウンロード
1. setup-x86_64.exe (64-bit installation)を選択し、実行
1. カテゴリで「full」を選択
1. 検索で「fish」と記載
1. fish と記載されたパッケージを「install」へ変更（ダブルクリック）

## ターミナル立ち上げ時のログインシェルの変更
1. 「passwd」を作成
```bash
$ mkpasswd > /etc/passwd
```
2. 自身のユーザのみ「/bin/fish」に書き換える 
```bash
$ emacs /etc/passwd
```

\#　通常のLinux環境では「chsh」を使用して簡単に設定できるが、CygwinやMinttyでは使用できないため、「/etc/passwd」にて設定する必要がある。