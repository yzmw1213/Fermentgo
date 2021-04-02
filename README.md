# Fermentgo
　自分の好きな発酵食品を共有するためのサービス

## 制作動機
　大学で生物・発酵工学を学習する傍、同世代の間で発酵食品の人気があまり高くない事に気付きました。
特に、私の地元の特産物である納豆は健康に良い事は漠然と分かっているものの、
「美味しくない」「臭い」などといった理由で若い世代から避けられている事がよくあります。

　そこで、発酵食品の魅力を発信し、共有するためのアプリケーションを作成しました。
納豆に限らず、乳酸菌やお酒などの食品が共有され、広がることを狙いとしています。

## 一般ユーザーログイン用認証情報
メールアドレス: test@exampleuser.com
パスワード: s8JhLsk3w7
※ ゲストアカウントログインのボタンからもログインできますが、
初期段階では作成済みの投稿は0件になるので、上記ユーザーでのログインをお勧めします。

## 使用技術 (詳細は各リポジトリのREADMEを参照)
- Go 1.15
- Nuxt 2.0.0
- TypeScript 3.8.3
- Docker,docker-compose
- protoc 3.11.0
- gRPC v1.31.0
- Envoy 1.16.1
- AWS, terraform
- CircleCI

## 構成図
![PortfolioArchitecture](https://user-images.githubusercontent.com/36359899/109421540-26e24200-7a1b-11eb-8871-b2a4c6723f05.png)

## 機能一覧
- 投稿、ユーザーサービス
  - 新規登録、編集、削除、全件取得、検索
  - タグ登録
  - 投稿タグ付け
  - 投稿お気に入り機能
  - 投稿コメント
  - ログインIDとパスワードによる認証・jwt発行
  - ユーザーフォロー
  - 簡単ログイン
  - 一般ユーザー、管理ユーザー権限
  - go-playground/validatorを用いたバリデーション

- サービス間通信
  - Envoyプロキシを介した他サービスとの通信

## アピールポイント
1. マイクロサービスアーキテクチャを採用している
2. gRPCでサービス間通信を行っている
3. goのテストコードを書いている
4. interfaceを書いてメソッドの実装チェックを行っている
5. SPAを採用している
6. TypeScriptを使い、型を制御している
7. linter, eslintを使っている
8. AWSインフラをコード化している
9. issueとプルリクエストを活用している
10. CircleCIでDockerfileのビルドを行い、本番環境を自動で更新している

## 関連レポジトリ
- [フロントエンド](https://github.com/yzmw1213/Front)
- [Envoyプロキシ](https://github.com/yzmw1213/Proxy)
- [投稿サービス](https://github.com/yzmw1213/PostService)
- [ユーザーサービス](https://github.com/yzmw1213/UserService)
- [AWSインフラ](https://github.com/yzmw1213/Infra)
