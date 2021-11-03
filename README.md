# GO言語環境構築
GO言語環境構築のためのファイル
## Docker コンテナ一覧
- api   : golang
- front : node
- nginx
- db    : mysql
- phpmyadmin
## 起動コマンド
### NEXT.js + TypeScript
`docker-compose run --rm front yarn install create-next-app`

`docker-compose run --rm front npx create-next-app [プロジェクト名] --ts`
### コンテナ起動
`docker-compose up -d`
### コンテナへ入る
`docker-compose exec [サービス名] [シェル]`
