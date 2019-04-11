# WordPress コミュニティハンドブック

こちらは [WordPress Community Handbooks](https://make.wordpress.org/community/handbook/) の翻訳用リポジトリです。

現在、[Meetup Organizer Handbook](https://github.com/jawordpressorg/community-handbook/tree/master/meetup-organizer) は翻訳済みですが、タイポや誤訳の修正を受け付けています。

[WordCamp Organizer Handbook](https://github.com/jawordpressorg/community-handbook/tree/master/wordcamp-organizer) については、このリポジトリ上以外で翻訳が完了しているものもありますので、[進捗シート](https://docs.google.com/spreadsheets/d/1q_d9JIpaXPhqvNBZIdHOmFsMUFIXHd3NqRu2wLgbFXM/edit#gid=0)をご覧ください。「優先順位」が「要」で、担当者が不在のものから始めていただけると助かります。

ブラウザ上で翻訳したい md ファイルをクリックし、鉛筆マークの「Edit this file」をクリックすることでブラウザ上でも更新 （プルリクエスト） できます。
GitHub が初めての方も[翻訳開始から提案までの流れ](https://github.com/jawordpressorg/community-handbook/wiki/%E7%BF%BB%E8%A8%B3%E9%96%8B%E5%A7%8B%E3%81%8B%E3%82%89%E6%8F%90%E6%A1%88%E3%81%BE%E3%81%A7%E3%81%AE%E6%B5%81%E3%82%8C)を参考に、ぜひご参加ください。

## 翻訳方法

__原文例：__

```
# Welcome
```

__手順：__

1.  __原文をコメントアウトします。__
    ```
    <!-- # Welcome -->
    ```
    _`<!--` の後ろと、`-->` の前には半角スペースを入れてください。翻訳の最小単位 (コメントアウトの単位) は段落 (空行から空行まで) でお願いします。_
2.  __コメントアウトした原文の下に翻訳を追加します。__
    ```
    <!-- # Welcome -->
    # ようこそ
    ```
3.  __`master` ブランチにプルリクエストします。__

## 進捗シート

[Meetup Organizer Handbook / WordCamp Organizer Handbook 翻訳の進捗シート](https://docs.google.com/spreadsheets/d/1q_d9JIpaXPhqvNBZIdHOmFsMUFIXHd3NqRu2wLgbFXM/edit#gid=629965050) に記入の上参加いただけますと進捗がわかりやすいのでご協力ください。

## 翻訳用語集・スタイルガイド

翻訳に悩んだ場合はまずこのコミュニティハンドブック翻訳専用の[用語集](https://github.com/jawordpressorg/community-handbook/blob/master/glossary.md)を参照してください。

また、WordPress プロジェクト全般向けの[翻訳スタイルガイド](https://wpdocs.osdn.jp/WordPress_%E3%81%AE%E7%BF%BB%E8%A8%B3/%E7%BF%BB%E8%A8%B3%E3%82%B9%E3%82%BF%E3%82%A4%E3%83%AB%E3%82%AC%E3%82%A4%E3%83%89)と[用語集](https://translate.wordpress.org/projects/wp/dev/ja/default/glossary)も活用してください。

## 原文追加・更新方法

1.  [`en` ブランチ](https://github.com/jawordpressorg/community-handbook/tree/en)をチェックアウトします。
2.  原文を更新します。
3.  [`en` ブランチ](https://github.com/jawordpressorg/community-handbook/tree/en)にプルリクエストします。

_`en` ブランチには翻訳を含めないでください。_
