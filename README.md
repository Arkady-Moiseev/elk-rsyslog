# Сбор и анализ логов

<b>Научится проектировать централизованный сбор логов. Рассмотреть особенности разных платформ для сбора логов.</b>
___
1) После подготовки ВМ и установки веб-сервера и elk приступаем к настройке центрального сервера сбора логов.
Редактируем <a href="https://github.com/Arkady1996/elk-rsyslog/blob/main/rsyslog.conf">rsyslog.conf</a>

2) Пропускаю шаги с установкой и настройкой ELK. Для сбора событий используются следующие конфиги logstash:
  <p>2.1 <a href="https://github.com/Arkady1996/elk-rsyslog/blob/main/01-winlogbeat-input.conf">01-winlogbeat-input.conf</a></p>
  <p>2.2 <a href="https://github.com/Arkady1996/elk-rsyslog/blob/main/02-linux-input.conf">02-linux-input.conf</a></p>
  <p>2.3 <a href="https://github.com/Arkady1996/elk-rsyslog/blob/main/03-nginx-syslog.conf">03-nginx-syslog.conf</a></p>
  
3) Правим конфиг веб-сервера для отправки событий.
  <p><a href="https://github.com/Arkady1996/elk-rsyslog/blob/main/nginx.conf">nginx.conf</a></p>
  
Далее правим конфиг auditd и устанавливаем плагин. Итог на скрине далее...

Централизованный сбор событий с помощью rsyslog:

![img_1](https://github.com/Arkady1996/elk-rsyslog/blob/main/images/rsyslog.PNG)

Auditd

![img_2](https://github.com/Arkady1996/elk-rsyslog/blob/main/images/auditd.PNG)
![img_2](https://github.com/Arkady1996/elk-rsyslog/blob/main/images/auditd2.PNG)

ELK

![img_3](https://github.com/Arkady1996/elk-rsyslog/blob/main/images/elk1.PNG)
![img_4](https://github.com/Arkady1996/elk-rsyslog/blob/main/images/elk2.PNG)
