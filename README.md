# SuperTelegramBot
Суть бота такая 
-> Пользователь отправляет сообщение в виде текста нашему боту

-> Это сообщение попадает в брокер RabbitMq, отправляет его отдельный микросервис, который принимает сообщения от брокера

-> В данном микросервисе сохраняется информация о пользователе, который отправил сообщение в таблицу

-> Дальше содержимое сообщения от пользователя отправляется либо на vk-api, либо на апишку chatGpt, после чего ловим ответ
от одной из этих апишек, парсим его и асинхронно отправляем содержимое ответа пользователю. 

-> В рамках вк апи это будет содержимое песни по названию трека; в рамках chatGpt это будет ответ нейронки на отправленное пользователем сообщение
