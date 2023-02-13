# LinuxIntro. Seminar 4. Homework
### Подключить дополнительный репозиторий на выбор: Docker, Nginx, Oracle MySQL
1. Следовал инструкциям по добавлению репозитория с сайта разработчика Docker. Проверил, действительно ли в соответствующем файле прописана строка с репозиторием   
![image](https://user-images.githubusercontent.com/108574612/218383887-62f11379-85ba-4e37-b438-8fc311108058.png)  
![image](https://user-images.githubusercontent.com/108574612/218383712-9ad01cea-3b82-4dea-90db-dcc21187814c.png)  
![image](https://user-images.githubusercontent.com/108574612/218384156-979934c7-b31d-4c93-a440-d06312ec5412.png)
![image](https://user-images.githubusercontent.com/108574612/218384635-8dc1cc3f-18d0-4015-b826-8dc6bd4c02af.png)
![image](https://user-images.githubusercontent.com/108574612/218384925-539fce9f-fd67-43cc-974d-36c0c6177c12.png)
---
### Установить и удалить deb-пакет с помощью dpkg
1. Скачал .deb с сайта разработчика  
![image](https://user-images.githubusercontent.com/108574612/218386196-f7f343e9-df4b-48c2-b7c8-563c86ed9888.png)  
2. Установил с помощью apt, чтобы автоматически подтянуть зависимости  
![image](https://user-images.githubusercontent.com/108574612/218387084-8dc38f06-5952-4d54-a87c-6174f09584ea.png)
---
### Установить и удалить snap-пакет
1. Установил snap-пакет  
![image](https://user-images.githubusercontent.com/108574612/218390249-b1633388-57a5-4e53-9084-52c8db60a86d.png)
2. Удалил snap-пакет  
![image](https://user-images.githubusercontent.com/108574612/218390730-e99ba651-46c0-4706-999d-8ee353bcf65d.png)
---
### Добавить задачу для выполнения каждые 3 минуты (создание директории, запись в файл)
1. Открыл свой файл-планировщик для редактирования и прописал задачу (добавлять строку в файл каждые 3 минуты)  
![image](https://user-images.githubusercontent.com/108574612/218391731-17a68900-5622-4ce3-9a2b-ae1380ff9eb7.png)  
![image](https://user-images.githubusercontent.com/108574612/218392271-cdaaa30d-d66a-4fd5-85e1-fb5eaef2c71a.png)  
![image](https://user-images.githubusercontent.com/108574612/218392331-251ddeaa-d7a2-47db-b339-a645c543ecac.png)  
![image](https://user-images.githubusercontent.com/108574612/218392727-1ce82b3c-2c05-4d93-be79-8322ea40e698.png)
---
### Подключить PPA-репозиторий на выбор. Установить из него пакет. Удалить PPA из системы
1. Добавил ppa-репозиторий в число отслеживаемых репозиториев  
![image](https://user-images.githubusercontent.com/108574612/218393568-b844f47e-c2e7-4a4f-aaa5-86dd666dffe0.png)
2. Установил пакет из ppa-репозитория  
![image](https://user-images.githubusercontent.com/108574612/218394054-d8879435-a2f9-4a4e-a1de-e2b2be746009.png)  
3. Удалил пакет  
![image](https://user-images.githubusercontent.com/108574612/218410669-ee03c8ba-4a16-4c99-abe9-30e53d7440d8.png)
4. Убрал ppa-репозиторий из числа отслеживаемых  
![image](https://user-images.githubusercontent.com/108574612/218411537-e7730450-4eb9-47e8-928b-55cf99fb270d.png)
---
### Создать задачу резервного копирования (tar) домашнего каталога пользователя. Реализовать с использованием пользовательских crontab-файлов
1. В файл-планировщик рута добавил задачу для резервного копирования директории /home каждые Пн и Чт в 23:59. Попробую добавить файлик для отслеживания, когда выполнились резервное копирование  
![image](https://user-images.githubusercontent.com/108574612/218414779-57f10045-5bb3-409f-a9ff-f28f30fbf620.png)    
![image](https://user-images.githubusercontent.com/108574612/218414409-fc4f9316-fb4a-4bc3-91d2-22229050b61c.png)  
![image](https://user-images.githubusercontent.com/108574612/218414886-e0228515-51e3-48b7-8745-ded34ac8158a.png)
---
P.S.  
echo с переменными (дата и время), почему-то срабатывает в терминале, но не работает в кронтабе. Может где-то напортачил...  
В общем, написал скриптик на пайтоне(для дозаписи даты и времени бэкапа в файл), и поставил его исполняться последней командой. Так всё сработало  
![image](https://user-images.githubusercontent.com/108574612/218572738-1a510634-f96a-4f89-9498-a70f9c45aa87.png)  
![image](https://user-images.githubusercontent.com/108574612/218574263-259806b8-a9ca-4c96-b88c-95c995977f15.png)  
Не очень понимаю насколько часто нужно бэкапы делать, но поставил два раза в неделю на ночь))







