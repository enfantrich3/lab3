# Отчет по лабораторной 3
Для выполнения задания лабораторной работы я скачала VMware Fusion и создала там три виртуальные машины linuxA linuxB и linuxC\
Затем в настройках сети я поставила Custom --> Private to my Mac\
Это используется для создания пользовательских сетей между виртуальными машинами и позволяет точно контролировать, как виртуальные машины взаимодействуют друг с другом и с внешними сетями.\
Переходим в виртуальную машину linuxA и проверяем доступ в интернет командой ping google.com\
<img width="570" alt="Снимок экрана 2024-11-14 в 14 12 07" src="https://github.com/user-attachments/assets/0cecf8b3-9ee7-46ee-baeb-2feb7ec522a7">\
По данному снимку экрана видно, что выход в интернет у виртуальной машины присутствует\
Далее таким же образом настраиваем виртуальные машины linuxB и linuxC, выставляя такие же настройки сети\
Перед началом выполнения заданий лабораторной работы необходимо выяснить IP-адреса виртуальных машин.\
Это можно сделать, прописав в терминале команду "ip a"\
<img width="869" alt="Снимок экрана 2024-11-28 в 14 13 58" src="https://github.com/user-attachments/assets/e65b5f29-8290-4aba-bb95-f4b7d92ac2c7">\
Таким образом IP-адрес машины linuxA 172.16.251.129\
Тоже самое делаем с машинами linuxB и linuxC\
<img width="832" alt="Снимок экрана 2024-11-28 в 16 25 42" src="https://github.com/user-attachments/assets/0b9608c0-41d8-414b-9c5e-de6ba5a5cf96">\
<img width="892" alt="Снимок экрана 2024-11-28 в 16 27 59" src="https://github.com/user-attachments/assets/67891096-fd1b-4b97-ad9e-96b01856f4ef">\
Теперь необходимо организовать сетевой доступ из виртуальной машины А в машину B\
Для этого в терминал машины А нужно ввести команду ping <IP-адрес машины B>\
<img width="738" alt="Снимок экрана 2024-11-28 в 14 27 53" src="https://github.com/user-attachments/assets/bc71373f-c6eb-4072-ac4c-c6c23b9465e4">\
Аналогично для доступа к машине С\
<img width="644" alt="Снимок экрана 2024-11-28 в 14 35 07" src="https://github.com/user-attachments/assets/36d444b7-c7bf-440b-bd85-6c360efd697b">\
Для того, чтобы запретить доступ из машины B в машину C нужно в терминал машины linuxC ввести команды "sudo ufw enable" и "sudo ufw deny from <IP-адрес машины B>", а затем проверить статус командой "sudo ufw status"\
<img width="902" alt="Снимок экрана 2024-11-28 в 14 39 43" src="https://github.com/user-attachments/assets/5c30dc05-a77c-473f-a1f3-2c0539cdc78a">\
Далее в терминале машины B вводим команду ping <IP-адрес машины C>\
<img width="641" alt="Снимок экрана 2024-11-28 в 14 56 54" src="https://github.com/user-attachments/assets/52999e89-093c-4a25-b869-e1cdf8fbd733">












