Laravel8とphp8で開発環境をすぐに構築するためのテンプレート

laravel8初期状態のコンテナです。
phpmyadminを入れて、php.iniのファイルサイズ上限だけ上げています。

ポート番号8080
phpmyadmainは8081

インストールしたいディレクトリに移動（ディレクトリごとダウンロードされるので新たにフォルダを作る必要はない）
git clone https://github.com/diepyon/laravel8andDocker.git

任意の名称に変更
mv laravel8andDocker newname

ディレクトリ内に移動して
docker compose up -d


インストール後に下記のコマンドが必要
docker compose exec app bash
composer install
cp .env.example .env
php artisan key:generate
php artisan storage:link
chmod -R 777 storage bootstrap/cache
php artisan migrate
exit

githubnの紐づけ直しも必要
git remote set-url origin {new-url}
git add -A
git commit -m "first commit"
git branch -M main
git push -u origin main
