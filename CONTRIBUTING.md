# プロジェクトに貢献する

[SoftwareCarpentry][swc-site]と[DataCarpentry][dc-site]はオープンソースのプロジェクトです。
コミュニティーからの資料提供・ご協力、例えば、
新しいレッスン、
既存の資料の修正、
バグレポート、
変更点のレビューなど、どんなに些細な変更も歓迎いたします。

## 貢献者の規約

このプロジェクトに貢献することにより、
自身が提供したコンテンツを[私達のライセンス](License.md)に基づき配布する事に同意するものとします。
ご協力と引き換えに、
私達はあなたが提供する変更点・問題点などを検討し、
できるだけ早くコミュニティーの一員になれるよう尽力いたします。
[Software Carpentry][swc-site]と[Data Carpentry][dc-site]の一員になられた際には、
私達の[行動規範](https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html)を遵守する事に同意していただきます。

## 貢献する方法

一番簡単に貢献する方法は、
誤字、言葉遣い、
間違った内容などを
issue(イシュー)で報告する事です。
Issueを報告することによって、自分をコミュニティーに紹介し、
また、コミュニティーのメンバーと出会う良い機会にもなります。

1. [GitHub][github]アカウントをお持ちでない場合、
    [メール][contact]にてご連絡して下さい。
    ですが、
    以下の方法であればメールよりも早急に対応できる場合がありますので、そちらをお勧め致します。

2. [GitHub][github]アカウントをすでにお持ちである方・
    またはアカウントを[新たに作る][github-join]気がある方で、
    あまりGitに詳しくない・使い慣れていない方は、
    質問・提案などを[新しいイシュー][new-issue]として開いて下さい。
    イシューを開くことによって、コミュニティーから誰かをそのイシューに割り当て、
    スレッド化したディスカッションとして質問・提案に応答させていただくことができます。

3. Gitを使い慣れている方で、
    既存の資料を変更、または追加したい方は、
    プルリクエスト(Pull Request)にて変更点を提出して下さい。
    プルリクエストを使った提出方法は、[下記に記載されています](#using-github)。

## どこへ貢献するか

1.  このレッスンの内容を変更したい場合は、
    <https://github.com/swcarpentry/git-novice>から編集して下さい。
    ウェブサイトはこちらから観覧いただけます：<https://swcarpentry.github.io/git-novice>

2.  模範レッスンの内容を変更したい場合は、
    <https://github.com/carpentries/lesson-example>から編集して下さい。
    このレポジトリは模範レッスンの内容を記載しており、
    こちらから観覧できます：<https://carpentries.github.io/lesson-example>.

3.  ワークショップのウェブサイトに使われるテンプレートの内容を変更したい場合は、
    <https://github.com/carpentries/workshop-template>から編集して下さい。
    このレポジトリのホームページに、ワークショップに使うウェブサイトの設立方法が記載されており、
    <https://carpentries.github.io/workshop-template>から
    サイトの詳細なデザイン方針が観覧できます。

4.  `_includes`、または`_layouts`に保存されている、レッスンやワークショップのためのCSSファイル、ツール、
    HTML boilerplateなどを編集したい場合は、
    <https://github.com/carpentries/styles>から編集して下さい。

## 貢献していただきたい個所

新しい例を書く、すでにある例の改善、
ドキュメントのアップデート、
不明瞭な点、欠点、「動作に不具合がある」といった
[バグの報告][new-issue]など、
様々な方法で貢献していただくことができます。
どういったイシューを開いたら良いかわからない場合は、
[このレポジトリのイシュー][issues]、
[Data Carpentryのイシュー][dc-issues]、
もしくは[Software Carpentryのイシュー][swc-issues]を見てみて下さい。

すでにあるイシューへのコメントや、プルリクエストのレビューなども歓迎いたします。
皆さんで協力したほうが、良い結果につながります。
また、新しく加入された方の意見やレビューなどは特に重要視しています。
レッスンの資料を幾度となく見てきた方は特に見落としがちなのですが、
私達が提供している資料・コンテンツは、初めて資料を見る方などには、理解するのに時間が掛かる場合があるので、
通常とは違う視点からの意見は大変貴重なのです。

## 貢献していただきたくない個所

Our lessons already contain more material than we can cover in a typical workshop,
so we are usually *not* looking for more concepts or tools to add to them.
As a rule,
if you want to introduce a new idea,
you must (a) estimate how long it will take to teach
and (b) explain what you would take out to make room for it.
The first encourages contributors to be honest about requirements;
the second, to think hard about priorities.

We are also not looking for exercises or other material that only run on one platform.
Our workshops typically contain a mixture of Windows, Mac OS X, and Linux users;
in order to be usable,
our lessons must run equally well on all three.

## Using GitHub

If you choose to contribute via GitHub,
you may want to look at
[How to Contribute to an Open Source Project on GitHub][how-contribute].
In brief:

1.  The published copy of the lesson is in the `gh-pages` branch of the repository
    (so that GitHub will regenerate it automatically).
    Please create all branches from that,
    and merge the [master repository][repo]'s `gh-pages` branch into your `gh-pages` branch
    before starting work.
    Please do *not* work directly in your `gh-pages` branch,
    since that will make it difficult for you to work on other contributions.

2.  We use [GitHub flow][github-flow] to manage changes:
    1.  Create a new branch in your desktop copy of this repository for each significant change.
    2.  Commit the change in that branch.
    3.  Push that branch to your fork of this repository on GitHub.
    4.  Submit a pull request from that branch to the [master repository][repo].
    5.  If you receive feedback,
        make changes on your desktop and push to your branch on GitHub:
        the pull request will update automatically.

Each lesson has two maintainers who review issues and pull requests
or encourage others to do so.
The maintainers are community volunteers,
and have final say over what gets merged into the lesson.

## Other Resources

General discussion of [Software Carpentry][swc-site] and [Data Carpentry][dc-site]
happens on the [discussion mailing list][discuss-list],
which everyone is welcome to join.
You can also [reach us by email][contact].

[contact]: mailto:team@carpentries.org
[dc-issues]: https://github.com/issues?q=user%3Adatacarpentry
[dc-lessons]: http://datacarpentry.org/lessons/
[dc-site]: http://datacarpentry.org/
[discuss-list]: https://carpentries.topicbox.com/groups/discuss
[github]: https://github.com
[github-flow]: https://guides.github.com/introduction/flow/
[github-join]: https://github.com/join
[how-contribute]: https://egghead.io/series/how-to-contribute-to-an-open-source-project-on-github
[new-issue]: https://github.com/swcarpentry/git-novice/issues/new
[issues]: https://github.com/swcarpentry/git-novice/issues/
[repo]: https://github.com/swcarpentry/git-novice/
[swc-issues]: https://github.com/issues?q=user%3Aswcarpentry
[swc-lessons]: https://software-carpentry.org/lessons/
[swc-site]: https://software-carpentry.org/

