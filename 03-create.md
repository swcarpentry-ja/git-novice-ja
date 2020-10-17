---
title: リポジトリの作成
teaching: 10
exercises: 0
questions:
- "Gitはどこに情報を格納しますか?"
objectives:
- "ローカルのGitリポジトリを作成する。"
keypoints:
- "`git init` はリポジトリを初期化する。"
- "Gitはリポジトリデータのすべてを`.git`ディレクトリに格納する。"
---

Gitの設定ができたら、
それを使い始めることができます。

まず、`Desktop`フォルダーに作業用のディレクトリを作成し、そのディレクトリに移動しましょう:

~~~
$ cd ~/Desktop
$ mkdir planets
$ cd planets
~~~
{: .language-bash}

次に、Gitに`planets`を[リポジトリ]({{ page.root }}/reference#repository)—
（Gitがファイルのバージョンを保存できる場所）にするように伝えます。

~~~
$ git init
~~~
{: .language-bash}

`ls` を使ってディレクトリの内容を表示すると、
何も変更されていないように見えます:

~~~
$ ls
~~~
{: .language-bash}

ですが `-a` フラグを追加してすべてを表示すると、
Git が `.git`という隠しディレクトリを `planets` の中に作ったことがわかります: 

~~~
$ ls -a
~~~
{: .language-bash}

~~~
.\t..\t.git
~~~
{: .output}

Git はプロジェクトのディレクトリ内にあるすべてのファイルとサブディレクトリを含む、プロジェクトに関するすべての情報を格納するためにこの特別なサブディレクトリを 使用します。
`.git` サブディレクトリを削除すると、
プロジェクトの履歴を失うことになります。

プロジェクトのステータスをGitに問うことで、
すべてが正しく設定されていることを確認できます:

~~~
$ git status
~~~
{: .language-bash}

使用している`git`のバージョンによって、
出力の表現が少し異なるかもしれません。

~~~
# On branch master
#
# Initial commit
#
nothing to commit (create/copy files and use "git add" to track)
~~~
{: .output}

> ## Git リポジトリを作る場所
>
> planets (すでに作成したプロジェクト) についての情報を追跡すると共に、 
> ドラキュラは moons についての情報も追跡したいと考えています。
> 狼男の心配にもかかわらず、ドラキュラは次の一連のコマンドを使って、彼の `planets` 
> プロジェクト内に `moons` プロジェクトを作ります:
>
> ~~~
> $ cd ~/Desktop   # Desktop ディレクトリに戻ります
> $ cd planets     # すでに Git リポジトリである planets ディレクトリ移動します
> $ ls -a          # .git サブディレクトリがまだ planets ディレクトリに存在することを確認します
> $ mkdir moons    # サブディレクトリ planets/moons を作ります
> $ cd moons       # moons サブディレクトリに移動します
> $ git init       # moons サブディレクトリをGitリポジトリにします
> $ ls -a          # .git サブディレクトリが存在し、新しいGitリポジトリが作られたと示していることを確認します。
> ~~~
> {: .language-bash}
>
> `git init` コマンドは、`moons` サブディレクトリ内で実行され、> `moons` サブディレクトリに保存されているファイルを追跡するために必要でしょうか?
> 
> > ## 解答
> >
> > いいえ。ドラキュラは `moons` サブディレクトリを Git リポジトリにする必要はありません。 
> > `planets` リポジトリは、`planets` ディレクトリの下のすべてのファイル、サブディレクトリ、> > およびサブディレクトリファイルを追跡するからです。従って、> > moons についてのすべての情報を追跡するのは、ドラキュラが `moons` サブディレクトリを> > `planets` ディレクトリに追加するだけで済みます。
> > 
> > それと、Git リポジトリが"入れ子にされている"場合、Gitリポジトリは互いに干渉する可能性があります:
> > 外側のリポジトリは内側のリポジトリのバージョン管理を
> > しようとします。したがって、新しいGitリポジトリはそれぞれ
> > 別のディレクトリに作るのがベストです。ディレクトリに競合するリポジトリが> > がないことを確認するには、`git status`の出力を確認します。次のような場合は、> > 上の方で示したように新しいリポジトリを作ることをお勧めします:
> >
> > ~~~
> > $ git status
> > ~~~
> > {: .language-bash}
> >
> > ~~~
> > fatal: Not a git repository (or any of the parent directories): .git
> > ~~~
> > {: .output}
> {: .solution}
{: .challenge}

> ## Correcting `git init` Mistakes
> ドラえもん explains to のび太 how a nested repository is redundant and may cause confusion
> down the road. のび太 would like to remove the nested repository. How can のび太 undo 
> his last `git init` in the `moons` sub-directory?
>
> > ## Solution -- USE WITH CAUTION!
> >
> > To recover from this little mistake, のび太 can just remove the `.git`
> > folder in the moons subdirectory by running the following command from inside the `planets` directory:
> >
> > ~~~
> > $ rm -rf moons/.git
> > ~~~
> > {: .language-bash}
> >
> > But be careful! Running this command in the wrong directory, will remove
> > the entire Git history of a project you might want to keep. Therefore, always check your current directory using the
> > command `pwd`.
> {: .solution}
{: .challenge}

