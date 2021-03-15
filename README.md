# philharmonia-burleske/website
フィルハーモニア・ブルレスケの Web サイトの資材管理用リポジトリです。
http://orchestra.musicinfo.co.jp/~burleske/

## Web サイトの更新方法
Web サイトの更新をしたい人が本リポジトリの `master` ブランチに更新をプッシュします。そちらをトリガーにして FTP デプロイ用の GitHub Actions ワークフローが起動し Web サイトに自動的に更新が反映されます。

- 本リポジトリ用 GitHub Actions ワークフロー 設定ファイル
    - https://github.com/philharmonia-burleske/website/blob/master/.github/workflows/main.yml
- 本リポジトリ用 GitHub Actions ワークフロー 実行履歴
    - https://github.com/philharmonia-burleske/website/actions

### 留意事項
- Web サイトの更新ができる人
    - `master` ブランチに更新をプッシュできるのは本リポジトリを所有する GitHub Organization [philharmonia-burleske](https://github.com/philharmonia-burleske) のメンバーです。
    - メンバーになる場合は GitHub のユーザーを作成した上で、Organization の既存のメンバーに招待を依頼してください。
- Web サイトの更新方法の使い分け
    - Web サイトの更新には原則、本リポジトリを利用ください。
    - [過去の演奏会のアーカイブ](http://orchestra.musicinfo.co.jp/~burleske/archive.html) は例外です。アーカイブの音声ファイル (mp3, wav など) はファイルサイズが大きいため、本リポジトリの管理対象外としています。アーカイブを更新したい場合は Web サーバーに直接 FTP で配置する必要があります。
    - Web サーバーの FTP 接続情報 (ホスト名、ユーザー、パスワード) は GitHub Secrets で暗号化して管理しており、そちらの Secrets を GitHub Actions ワークフローで参照するようにしています。FTP 接続情報は関係者に別途連絡します。
