---
layout: lesson
root: .
---

ドラえもんとのび太はに火星に惑星無人探査機を送ることができるかどうか、
検討するためにユニバーサル・ミッションズ（ユーフォーリック州立大学の
スピンオフ宇宙サービス）に雇われました。 彼らはそれぞれ同時に計画を
作りたいのですが、前にもこのような仕事をしようとしたら困ったことが
ありました。一人ずつするにと、待っている時間がもったいないですが、
それぞれ自分のコピーを編集して、メールで添付ファイルを送ったりすると
情報の喪失や上書き、複製などといった問題が起こります。

同僚は、[バーションの管理は]({{page.root}} / reference＃version-control)を使って作業を
管理することを提案しています。 バーションの管理を使うはファイルを前後にメールするよりも優れています：

*   本当に消そうとしない限り、バージョン管理にコミットされているものは
    失われることはありません。古いバージョンのファイルは
    すべて保存されているため、特定の日に誰が何を書き込んだのか、
    特定の結果を生成するためにどのバージョンのプログラムが使用されたのかなど、
    正確に確認することが可能です。

*   誰が何をいつ変更したのかという記録があるため、後に問題が
    生じた場合、連絡するべき人が分かる上に必要に応じて
    "元に戻す"機能のように、以前のバージョンに戻すことができます。

*   同じプロジェクトで複数の人が協力し合う場合、
    間違って誰かの変更を見落としたり上書きしたりする可能性があります。
    バージョン管理システムは、二つの変更点の間に不一致がある場合、
    自動的にユーザーに知らせてくれます。

バージョン管理を使うことによって得をするのはチームだけではありません: 個人で作業をしている
研究者にもメリットがあります。何が、いつ、何故変わったのかを
記録しておくことは、後で昔のプロジェクトを見返すことになった場合などに
（例えば、1年後、プロジェクトの詳細を忘れてしまった時などに）、
非常に便利です。

Version control is the lab notebook of the digital world: it's what
professionals use to keep track of what they've done and to
collaborate with other people.  Every large software development
project relies on it, and most programmers use it for their small jobs
as well.  And it isn't just for software: books,
papers, small data sets, and anything that changes over time or needs
to be shared can and should be stored in a version control system.

> ## Prerequisites
>
> In this lesson we use Git from the Unix Shell.
> Some previous experience with the shell is expected,
> *but isn't mandatory*.
{: .prereq}

