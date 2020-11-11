---
title: Git の設定
teaching: 5
exercises: 0
questions:
- Git を使うために必要な設定は何ですか？
objectives: 
- コンピュータで初めて `git` を使うための設定が出来るようになりましょう。
- `--global` 設定フラグの意味を理解しましょう。
keypoints:
-   "`git config` と `--global` オプションを使い、ユーザー名
メールアドレス、エディタ、その他の設定を行う。---

Git を新しいパソコンで初めて使う場合、
いくつかの設定を変更しなければなりません。Git を始めるにあたって、
私達が変更する設定をいくつか表記します：

*   名前とメールアドレス、
*   使用したいテキストエディタ、
*   以上の設定をグローバル設定として使う（つまり、全てのプロジェクトに反映させる）。

コマンドラインでは、Git コマンドは `git <動詞>` と入力します。
ここでの「動詞」は、Git に何をさせたいのかを表します。ドラキュラが新しいユーザーの場合、
以下のようにコンピュータを設定します：

~~~
$ git config --global user.name "Vlad Dracula"
$ git config --global user.email "vlad@tran.sylvan.ia"
~~~
{: .language-bash}

ここでは、ドラキュラの代わりに自分の名前とメールアドレスを使いましょう。ここで入力した名前とメールアドレスは、これから行う Git での作業に関わってきます。
というのも、これからのレッスンで
[GitHub](https://github.com/)、
[BitBucket](https://bitbucket.org/)、
[GitLab](https://gitlab.com/)、または
その他の Git をホストするサーバーに
変更箇所を「プッシュ」した（送った）際に、これらの情報が使われるからです。

> ## 改行コード
>
> 他のキーと同様に、<kbd>Return</kbd> キーを押すと、
> コンピュータはそれを文字として入力します。
> 話が長くなるので詳しい説明は省きますが、行末に使われる文字は
> オペレーティングシステム（OS）よって違います。
> （行末に使われる文字を「改行コード」と呼びます。）
> Git は、改行コードを使ってファイルの違いを確かめるため、
> 違うパソコンでファイルを編集した時に思わぬ問題が起こるかもしれません。
>
> Git がどのように改行コードを理解・変換するかは、
> `git config` の `core.autocrlf` コマンドを使って変更できます。
> 以下の設定をおすすめします：
>
> MacOS と Linux：
>
> ~~~
> $ git config --global core.autocrlf input
> ~~~
> {: .language-bash}
>
> Windows：
>
> ~~~
> $ git config --global core.autocrlf true
> ~~~
> {: .language-bash}
> 
> この問題についてもっと詳しく知りたければ、 
> [こちらの GitHub ページ](https://help.github.com/articles/dealing-with-line-endings/)
を参照してください。
{: .callout}

これらのレッスンでは、[GitHub](https://github.com/) に接続するので、GitHub アカウントと同じメールアドレスに設定してください。プライバシーについて気になる方は、[GitHub のメールアドレスをプライベートにするための説明][git-privacy] を参照してください。
GitHub が提供するプライベートメールアドレスを使う場合は、同じメールアドレスを `user.email` の値に設定してください（例：`username@users.noreply.github.com`）。メールアドレスは `git config` コマンドでいつでも変えることができます。

以下の表を参考に、ドラキュラはテキストエディタも設定しました：

| エディタ             | 設定コマンド                            |
|:-------------------|:-------------------------------------------------|
| Atom | `$ git config --global core.editor "atom --wait"`|
| nano               | `$ git config --global core.editor "nano -w"`    |
| BBEdit (Mac, with command line tools) | `$ git config --global core.editor "bbedit -w"`    |
| Sublime Text (Mac) | `$ git config --global core.editor "/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl -n -w"` |
| Sublime Text (Win, 32-bit install) | `$ git config --global core.editor "'c:/program files (x86)/sublime text 3/sublime_text.exe' -w"` |
| Sublime Text (Win, 64-bit install) | `$ git config --global core.editor "'c:/program files/sublime text 3/sublime_text.exe' -w"` |
| Notepad++ (Win, 32-bit install)    | `$ git config --global core.editor "'c:/program files (x86)/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Notepad++ (Win, 64-bit install)    | `$ git config --global core.editor "'c:/program files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`|
| Kate (Linux)       | `$ git config --global core.editor "kate"`       |
| Gedit (Linux)      | `$ git config --global core.editor "gedit --wait --new-window"`   |
| Scratch (Linux)       | `$ git config --global core.editor "scratch-text-editor"`  |
| Emacs              | `$ git config --global core.editor "emacs"`   |
| Vim                | `$ git config --global core.editor "vim"`   |

設定したテキストエディタもいつでも変更することができます。

> ## Vim の終了の仕方
>
> 多くのソフトの初期設定では、Vim がデフォルトのテキストエディタに設定されています。保存せずに Vim を終了するには、
 <kbd>Esc</kbd> キーを押した後に `:q!` と入力してから <kbd>Return</kbd> キーを押してください。
> 保存してから終了するには、 <kbd>Esc</kbd> キーを押してから `:wq` と入力して <kbd>Return</kbd> キーを押してください。
{: .callout}

上記の4つのコマンドは、一度実行するだけで十分です。`--global` フラグは Git に、
今使っているパソコン内にある自分のアカウントに関連する全てのプロジェクトに同じ設定をするように指示しています。

自分の設定はいつでも確認できます：

~~~
$ git config --list
~~~
{: .language-bash}

これらの設定はいつでも変えることができます。
以前使ったコマンドを使えば、違うエディタやメールアドレスに変えることができます。

> ## プロキシ
>
> ネットワーク環境によっては
> [プロキシ](https://en.wikipedia.org/wiki/Proxy_server) を使わなければならないかもしれません。
> この場合、プロキシの設定が必要です：
>
> ~~~
> $ git config --global http.proxy proxy-url
> $ git config --global https.proxy proxy-url
> ~~~
> {: .language-bash}
>
> プロキシを無効にするには：
>
> ~~~
> $ git config --global --unset http.proxy
> $ git config --global --unset https.proxy
> ~~~
> {: .language-bash}
{: .callout}

> ## Git のヘルプとマニュアル
>
> `git` のコマンドを忘れた時は、`-h` を使えばコマンドの一覧を、`--help` を使えばマニュアルを見ることができます：
>
> ~~~
> $ git config -h
> $ git config --help
> ~~~
> {: .language-bash}
{: .callout}

[git-privacy]: https://help.github.com/articles/keeping-your-email-address-private/

