# Моему сайту нужен HTTPS?
## ДА! ТВОЕМУ САЙТУ НУЖЕН HTTPS.

### Но на моем сайте не происходит сбора пользовательской информации и нет форм

> Не важно. HTTPS защищает больше, чем просто данные, передаваемые через формы! HTTPS сохраняет конфиденциальность ссылок, заголовков и содержимого всех страниц, по которым вы переходите.

### В любом случае, на моем сайте нет ничего важного

> Не важно. Вы отвечаете за свой сайт, соответственно и за то, что на нём отображается. Известно много случаев когда компании размещали свой код на страницах сайтов, без предупреждения. Вы действительно хотите чтобы, на вашем сайте были сторонние скрипты, изображения, реклама, а главное - чтобы все выглядело так, будто вы это все туда вставили? Примеров подобного много, например [компания Tele2](https://vc.ru/35975-tele2-stal-pokazyvat-polzovatelyam-mobilnogo-interneta-svoi-bannery-poverh-chuzhih-saytov), а также [билайн, мтс и мегафон](https://meduza.io/slides/mobilnye-operatory-podsovyvayut-abonentam-bannery-i-podpiski-na-platnye-sayty-kak-ot-nih-otkazatsya).

### У меня нет денег на SSL-сертификат

> [Вот тут](https://letsencrypt.org/) бесплатный.

### HTTPS сложно настроить и поддерживать

> Не сложно! Используйте веб-сервер [Caddy](https://caddyserver.com/), он автоматически выпустит и будет продлевать сертификат для вашего сайта. Для других случаев используйте [автоматизированный клиент Let's Encrypt](https://letsencrypt.org/docs/client-options/). Никаких особых технических знаний не потребуется.

### HTTPS это медленно

> [Нет, это не так](https://istlsfastyet.com/). Сайты на современных веб-серверах загружаются быстрее через HTTPS, чем без, благодаря HTTP/2.

### Сайт отлично работает на HTTP

> В последнее время [браузеры помечают такие сайты](https://habr.com/company/globalsign/blog/349428/) как небезопасные.

### Мой сайт доступен только внутри страны или через VPN

> Насколько вы доверяете своему [VPN провайдеру](https://www.securitylab.ru/news/488966.php)? А компании производящей сетевое оборудование?

### Мы шифруем пароли

> Это хорошо. Но это не поможет при [атаке "человек посередине" (mitm)](https://ru.wikipedia.org/wiki/%D0%90%D1%82%D0%B0%D0%BA%D0%B0_%D0%BF%D0%BE%D1%81%D1%80%D0%B5%D0%B4%D0%BD%D0%B8%D0%BA%D0%B0) если сайт будет работать по http и злоумышленники смогут перехватить пароли или их хеши. Пароли крадут не с вашей базы, а «из браузера пользователя».

### HTTPS вреден для SEO

> Неправильный переход с HTTP на HTTPS может повлиять на ранжирование, но это не отменяет того что, [поисковые системы рекомендуют использовать https](https://support.google.com/webmasters/answer/6073543?hl=ru). Просто настройте редирект правильным образом в соответствии с правилами поисковой системы и все будет хорошо.

### Это обязанность браузера, обеспечивать безопасность пользователей

> Правда, но не совсем. Это НЕ ТОЛЬКО обязанность браузера. Браузер может обеспечить безопасное соединение только при условии предоставления сервером защищённого соединения, что уже полностью ваша забота.

## КАК НАЧАТЬ ИСПОЛЬЗОВАТЬ HTTPS

Самый простой способ это [Let's Encrypt](https://letsencrypt.org/) или [веб-сервер Caddy](https://caddyserver.com/), они автоматически включат HTTPS для всех ваших сайтов. Вы также можете использовать простой кроссплатформенный автоматизированный клиент Let's Encrypt под названием [lego](https://github.com/xenolf/lego).  
  
Если вам требуется больше возможностей при настройки и интеграция с другими веб-серверами используйте, EFF's клиент [Certbot](https://certbot.eff.org/).  
  
Есть также множество других способов подключить HTTPS без особых проблем. Например, используя CDN сервис [Cloudflare](https://www.cloudflare.com/ssl/).
