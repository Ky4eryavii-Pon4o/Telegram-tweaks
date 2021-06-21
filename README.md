---
layout: default

---
<h4>Web Telegram</h4>
New

```
https://web.telegram.org/k/
```

New

```
https://web.telegram.org/z/
```
Legacy web telegram

```
https://web.telegram.org/?legacy=1#/im
```



<h4>Telegram</h4>
🤖 **Telegram bot (полезное)**

```
https://api.telegram.org/bot[token]/getUpdates 
```
где [token] это API который выдал BotFather.

Для отправки сообщения в чат, нужно использовать следующий URL:
```
https://api.telegram.org/bot[token]/sendMessage?chat_id=[chat_id]&text=[text]
```
Где:
[token] — это API который выдал @BotFather
[chat_id] — это ID вашего чата с ботом.

Например:
```
curl -s -X POST https://api.telegram.org/bot944496485:AAEtGaGCVrQ7d26Rc3r_cqXPIhrKVokh8e4/sendMessage 
-d chat_id=336116180 -d text="текст_сообщения"
````
[chat_id] - может быть с минусом перед цыфрами. Можно использовать ID группы.

<hr>

<h4>Telegram X theme</h4>

🎨 tgx-theme by Ky4eryavii_Pon4o/Patap


[Greeny_Gray.tgx-theme](https://github.com/Ky4eryavii-Pon4o/Telegram-tweaks/blob/master/Greeny_Gray.tgx-theme)

color: green/lime/orange/gray



