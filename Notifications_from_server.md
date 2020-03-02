<h4>Telegram, отправка уведомлений с сервера</h4>

С помощью созданного бота и полученных ID можно отсылать с сервера уведомления в Telegram чат, и таким образом получать какие-то интересные нам данные или алерты.

Для отправки сообщения в чат, нужно использовать следующий URL

<code>https://api.telegram.org/bot[token]/sendMessage?chat_id=[chat_id]&text=[text]</code>
Где:
[token] — это API который выдал @BotFather
[chat_id] — это ID вашего чата с ботом

Например:

<code>curl -s -X POST https://api.telegram.org/bot944496485:AAEtGaGCVrQ7d26Rc3r_cqXPIhrKVokh8e4/sendMessage -d chat_id=336116180 -d text="Доброе утро, страна"</code>

отправка сообщений в telegram бот через api и url

Для чего можно использовать такие Telegram уведомления? Например, при создании резервной копии вы можете отправлять уведомления о ее создании или же отправлять ссылку на скачивание копии в чат с ботом. Вы можете отправлять себе в Telegram уведомления с информацией о сбоях в системе. Можно добавить в крон выполнение каких-либо проверок с последующей отправкой в Telegram.

Еще пример использования подобных уведомлений:

<code>curl -s -X POST https://api.telegram.org/bot944496485:AAEtGaGCVrQ7d26Rc3r_cqXPIhrKVokh8e4/sendMessage -d chat_id=336116180 -d text=" User $(whoami) logged into $(hostname) on $(date) from $(echo $SSH_CLIENT | awk '{ print $1}')" &>/dev/null 2>&1</code>

Добавьте этот код в /etc/profile и будете получать уведомления в Telegram при каждом входе пользователей на сервер:

отправка сообщений в telegram через post и curl

Хочу напомнить, что во всех командах, нужно указывать именно своей token(API) и ID чата.
