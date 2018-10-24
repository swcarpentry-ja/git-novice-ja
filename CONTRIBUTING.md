# 貢献しています

[Software Carpentry] [swc-site]と[Data Carpentry] [dc-site]は
オープンソースのプロジェクトであり、あらゆる種類の貢献を歓迎します：
新しいレッスン、既存の資料への修正、
バグレポート、提案された変更のレビューは大歓迎です。

## 貢献者の協定

貢献することにより、あなたは[私たちの免許]（LICENSE.md）に基づいてあなたの仕事を再配布することに同意します。 引き換えに、
私たちはあなたの問題に対処し、あなたの変更提案をできるだけ早く評価し、あなたが私たちのコミュニティの一員になるのを手伝います。 [Software Carpentry] [swc-site]と[Data Carpentry] [dc-site]に関わる全員が、私たちの[行動規範](https://docs.carpentries.org/topic_folders/policies/code-of -conduct.html)を遵守することに同意します。

## 貢献する方法

始める最も簡単な方法は、スペルミス、不愉快な言葉遣い、
または事実の誤りについて私たちに知らせるために問題を提出することです。
 これはあなた自身を紹介し、コミュニティメンバーの
一部と出会うための良い方法です。

1. [GitHub] [github]アカウントをお持たなかったら、
あなたは[私たちにメールでコメントを送る] [連絡先]をすることができます。
でも、以下のいずれかの方法を使用すると、より迅速に対応することができます。

2. [GitHub] [github]アカウントを持っているかを[作たい][gitub-join]だったら、
Gitの使い方がしらなくて、
[issueを発行] [new-issue]で問題を報告するか
改善を提案することができます。 誰かにアイテムを
割り当て、スレッド化したディスカッションでそれに
応答するのは私たちのためです。

3. Gitを使いやすく、マテリアルを追加または変更したいだったら、
資料を追加または変更したいとき、
プルリクエスト(PR)を提出できます。
 これを行うための手順は[以下のとお](#using-github)。

## 貢献するどこ

1.  If you wish to change this lesson,
    please work in <https://github.com/swcarpentry/git-novice>,
    which can be viewed at <https://swcarpentry.github.io/git-novice>.

2.  If you wish to change the example lesson,
    please work in <https://github.com/carpentries/lesson-example>,
    which documents the format of our lessons
    and can be viewed at <https://carpentries.github.io/lesson-example>.

3.  If you wish to change the template used for workshop websites,
    please work in <https://github.com/carpentries/workshop-template>.
    The home page of that repository explains how to set up workshop websites,
    while the extra pages in <https://carpentries.github.io/workshop-template>
    provide more background on our design choices.

4.  If you wish to change CSS style files, tools,
    or HTML boilerplate for lessons or workshops stored in `_includes` or `_layouts`,
    please work in <https://github.com/carpentries/styles>.

## 何を貢献します

There are many ways to contribute,
from writing new exercises and improving existing ones
to updating or filling in the documentation
and submitting [bug reports][new-issue]
about things that don't work, aren't clear, or are missing.
If you are looking for ideas,
please see [the list of issues for this repository][issues],
or the issues for [Data Carpentry][dc-issues]
and [Software Carpentry][swc-issues] projects.

Comments on issues and reviews of pull requests are just as welcome:
we are smarter together than we are on our own.
Reviews from novices and newcomers are particularly valuable:
it's easy for people who have been using these lessons for a while
to forget how impenetrable some of this material can be,
so fresh eyes are always welcome.

## 何を貢献する要りません

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

