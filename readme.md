### Учебный вариант интернет-магазина ishoplite на языке ruby с использованием фреймворка sinatra
  все данные хранятся в файлах формата **_json_** в директории **databases**
  1. **db.json** - здесь лежит информация о товарах
  2. **users.json** - тут информация о пользователях
  3. **purchases.json** - информация о всех покупках: кто, когда и сколько
  4. **strings.json** - тут, в структурированном виде, находятся сообщения, которые выводятся на экран магазина в случае удачных или неудачных действий

в директории **public** лежат картинки товаров и те, что используются для прорисовки сайта, а также таблица стилей сайта в поддиректории **public/css**

директория **views** содержит шаблоны erb. Их несколько:
    - basket.erb - шаблон отображения корзины покупок
    - edit.erb   - шаблон для добавления, изменения, удаления товаров из/в базе. Доступен только пользователю **admin**
    - index.erb  - шаблон центрального блока, в котором отображается список всех товаров магазина
    - info.erb   - шаблон информации о товаре с интерактивными кнопками добавлления товара в корзину
    - layout.erb - основной шаблон сайта, так сказать макет, который использует все остальные шаблоны
    - login.erb  - шаблон авторизации в магазине
    - purchases.erb - шаблон списка всех покупок, доступен только пользователю admin из шаблона edit.erb
    - registration.erb - шаблон формы регистрации в магазине
    - users.erb  - шаблон управления и отображения пользователей магазина

Если авторизаваться под **admin**, то становится доступен интефейс администрирования базой товаров и пользователями, а также становиться возможным просматривать купленные товары. Навигация в администраторский интерфейс находится в нижней части сайта в меню Admin

Основная программа находится в файле **scripts.rb**
она запускается командой:

      ruby scripts.rb

Файлы **Gemfile**, **Procfile**, **Gemfile.lock** **config.ru**, **.env** нужны для развертывания приложения на облачном сервисе heroku.com

Проверить работу магазина можно на облачном сервисе heroku.com перейдя по адресу:
[https://ishoplite.herokuapp.com][ee7afcb2]

  [ee7afcb2]: https://ishoplite.herokuapp.com "https://ishoplite.herokuapp.com"
