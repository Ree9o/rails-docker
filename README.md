# README

## 環境構築方法
dockerとdocker-composeがすでにインストールしていると仮定して説明を行っています。
インストールされていない方は事前にインストールをお願いします。
### git-clone を行う

ディレクトリを作成し、当リポジトリを clone します。
`$ git clone https://github.com/Ree9o/rails_docker_template.git`

### docker-compose build を行う

docker-compose を採用していますので、`$docker-compose build`を行います。

### docker-compose up を行う

build が問題なく終了しましたら、`$docker-compose up`を行い、web と db コンテナを建ち上げます。

### Rails データベースの作成

rails でデータベースを作成します。`$docker-compose run web rake db:create`で作成できます。

### migrate する

データベースを作成できたら migrate を行います。`$docker-compose exec web bash`でターミナルを起動し、`$rails db:migrate`を行います。以上で環境構築が完了です。
