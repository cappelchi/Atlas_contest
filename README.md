# Atlas_contest
2 задачи с примерами и вводными данными, а также информацией по необходимому ПО.

![Analyse](https://github.com/cappelchi/Atlas_contest/blob/master/img/Atlas_contest2_plot3.png)

https://habr.com/ru/company/atlasbiomed/blog/480954/

https://habr.com/ru/company/atlasbiomed/blog/481334/

Дисклеймер
Работа с генетическими данными проводится на Unix системах (Linux, macOS), так как некоторые команды и ПО недоступны на Windows. Поэтому для пользователей Windows одним из самых простых решений будет арендовать виртуальную машину с Linux.

Все описанные ниже операции выполняются в командной строке — терминале. Перед началом выполнения узнайте, как работать в терминале под управлением вашей ОС и использовать команды, так как некоторые из них могут потенциально навредить ОС и вашим данным.


Необходимое ПО

Мы собрали образ виртуальной машины (ВМ) со всем необходимым ПО на Яндекс.Облаке. Зарегистрируйтесь в Яндекс.Облаке, в личном кабинете в разделе Compute Cloud нажмите «Создать ВМ». В качестве публичного образа выберите из каталога «Атлас Анализ Данных 1000 Геномов».

Конфигурация ВМ: 100% 2vCPU, 8GB RAM, 20GB HDD. При создании ВМ необходимо ввести платежные данные, но со счета ничего не спишется. Стартового и дополнительного гранта по кодовому слову достаточно, чтобы работать c ВМ и образом от Атласа до 31 декабря 2019 года бесплатно. Чтобы получить грант на прохождение задач, отправьте службе поддержки Яндекс.Облака кодовое слово «АТЛАС».

Примечание: грант действителен для новых пользователей Яндекс.Облака, которые завели аккаунт с 18 декабря 2019 года или для тех, у кого еще действует пробный период и имеется стартовый грант. Кодовое слово «АТЛАС» действует только один раз.

Предварительно создайте ssh ключ на локальном компьютере, с которого вы планируете подключаться к ВМ:

ssh-keygen -o -t rsa -b 4096 -C "my-local-machine" -f ~/.ssh/yandex-cloud -a 100

Не забудьте скопировать содержимое ~/.ssh/yandex-cloud.pub файла в соответствующее окно при создании ВМ.

Если вы хотите установить ПО на свой компьютер, ниже есть вся информация по установке. Если вы решили воспользоваться Яндекс.Облаком — создайте ВМ и переходите к следующему разделу.
