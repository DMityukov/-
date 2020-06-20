Во-первых, вы должны клонировать хранилище. Если у вас есть ключи ssh, используйте следующую команду в терминале «git clone git@github.com : Hidgi / pig.git», иначе используйте «git clone https://github.com/Hidgi/pig.git » (рекомендуется добавьте в файл gitignore строку "/ api / vendor /" для загрузки уже загруженных пакетов с помощью composer +, если вы будете использовать git flow, сделайте в репозитории "git init")

Перед началом установки вы должны обновить ваши пакеты в Ubuntu, используя приведенную ниже команду «sudo apt-get update»

Установите apache2 "sudo apt-get install apache2". перейдите в браузер и введите http: // localhost (или адрес сервера - зависит от того, что вы используете) для проверки успешной установки apache2 или нет.

Установите MySQL и выполните безопасную установку, выполнив следующие команды: «sudo apt-get install mysql-server» «mysql_secure_installation»

Установите PHP7.2 и важное расширение, используя там инструкцию " https://hostadvice.com/how-to/how-to-install-php7-2-on-ubuntu-18-04/ "

Установите PHPMyAdmin "sudo apt-get install phpmyadmin"

Для редактирования файла apache используйте vim с помощью команд "sudo apt-get install vim", "cd / etc / apache2 /", "sudo vim apache2.conf" и добавьте в последнюю строку "Include /etc/phpmyadmin/apache.conf" после этого перезапустите сервер apache "sudo service apache2 restart"

Установите Composer, руководствуясь здесь « https://getcomposer.org/download/ » и используйте команду «Установка композитора»

используйте «nano /etc/apache2/sites-available/000-default.conf» и перепишите туда «/ var / www» в «адрес хранилища» (если вы переместили файлы в «корневое пространство», выполните «mv currency-exchangng ~»). Если после этого у вас возникнут проблемы, используйте команды "a2ensite 000-default" и "sudo systemctl restart apache2"

если у вас возникли проблемы, рекомендуем проверить это руководство по установке веб-сервера https://www.pontin.ru/technical/linux/web-server-ubuntu

Для настройки phpmyadmin попробуйте использовать https://serverfault.com/questions/144095/phpmyadmin-on-ubuntu-lamp-login-without-a-password-is-forbidden-by-configurat, а это - https://devanswers.co / PHPMyAdmin-доступа отказано, для пользователей-корневого локального хоста /

У API есть два варианта: получить названия всех доступных валют - «получить / валюты» и получить цены валют - «получить / валюты / цены». Вы можете проверить API в файле Swager_description.yaml или по ссылке https://app.swaggerhub.com/apis/Kr0GG/Currencies-api/0.0.1/.

С этими советами вы можете использовать проект. Хорошего дня!
