laravel8������Ԃ̃R���e�i�ł��B
phpmyadmin�����āAphp.ini�̃t�@�C���T�C�Y��������グ�Ă��܂��B

�|�[�g�ԍ�8080
phpmyadmain��8081

�C���X�g�[����ɉ��L�̃R�}���h���K�v
docker compose exec app bash
composer install
cp .env.example .env
php artisan key:generate
php artisan storage:link
chmod -R 777 storage bootstrap/cache
php artisan migrate
exit