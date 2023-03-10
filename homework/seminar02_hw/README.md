# LinuxIntro. Seminar 2. Homework
### Используя команду cat, создать два файла с данными, а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя  
1. В **домашнем каталоге пользователя** создал директорию **homework**, в ней создал ещё одну: **seminar2**
![image](https://user-images.githubusercontent.com/108574612/215724778-056dce84-c0d4-482c-a6ca-b8f9cbc581ba.png)
2. Перешёл в директорию **seminar2**, создал **file1** и **file2**, записав в них какие-нибудь данные
![image](https://user-images.githubusercontent.com/108574612/215727635-dde87192-32f0-4765-97a7-70aa20273772.png)
3. Объединил **file1** и **file2** в **file3** и вывел его содержимое  
![image](https://user-images.githubusercontent.com/108574612/215729254-baaf5345-53b3-4b98-b4e5-e4e23958c42e.png)
4. Переименовал **file3** в **file_all** и, чтобы убедиться в результате, вывел список файлов в директории
![image](https://user-images.githubusercontent.com/108574612/215730457-3ab6ded3-b14e-4839-ba21-d0b2ac368057.png)
---
### Создать несколько файлов. Создать директорию, переместить файл туда. Удалить все созданные в этом и предыдущем задании директории и файлы
1. В той же директории создал пустые файлы **file3** и **file4**, создал директорию **new_dir** и переместил эти файлы в неё
![image](https://user-images.githubusercontent.com/108574612/215735947-bd790510-6571-46ab-bd96-07e568a4fc73.png)
2. Перешел в **домашний каталог пользователя** и рекурсивно удалил директорию **homework**
![image](https://user-images.githubusercontent.com/108574612/215736956-c5fd52af-8bd7-439d-82c9-249bea13575a.png)
---
### Создать файл file1 и наполнить его произвольным содержимым. Скопировать его в file2. Создать символическую ссылку file3 на file1. Создать жесткую ссылку file4 на file1. Посмотреть, какие айноды у файлов. Удалить file1. Что стало с остальными созданными файлами? Попробовать вывести их на экран.
1. В **домашнем каталоге пользователя** создал директорию **homework**, в ней создал ещё одну: **seminar2**. В директории **seminar2** создал **file1** с каким-нибудь содержимым  
![image](https://user-images.githubusercontent.com/108574612/215739489-a699de66-1f3f-491d-9e05-5ba9783ebb38.png)
2. Скопировал **file1** в **file2**. Создал символическую ссылку **file3** на **file1** и жесткую ссылку **file4** на **file1**. Вывел список файлов директории с указанием айнодов  
![image](https://user-images.githubusercontent.com/108574612/215741520-4b01e096-e07f-4dad-9d31-6da376eed8f5.png)
3. Удалил **file1**. Поочередно попробовал вывести содержимое **file2**, **file3**, **file4**  
![image](https://user-images.githubusercontent.com/108574612/215742816-8bb8662e-bba4-411a-befd-07877dc611ca.png)
4. Что стало с остальными файлами после удаления file1:
  - **file2** (копия) даже не заметил удаления, так как в процессе копирования он получил собственный айнод и идентиченое первому файлу собственное содержимое. Это как клонировать овечку: вот они, вроде, идентичные, но связи между ними никакой нет
  - **file3** (мягкая ссылка) потерпел наибольший ущерб из всех оставшихся. По сути он хранил в себе путь до первого файла. Если приводить аналогии из жизни: вот у меня есть карта сокровищ, я знаю как туда дойти и могу кого угодно туда отправить, но я становлюсь бесполезен, если эти сокровища каким-либо образом пропали из того места, которое отмечено на моей карте
  - **file4** (жесткая ссылка) сложнее всего объяснить. Имя файла в Линукс это лишь ссылка на какое-то нечто в памяти. При создании **file4** он стал ссылаться на то же самое нечто, что и **file1**. Удалив **file1**, мы больше не сможем обратиться по ссылке **file1** к этому нечто, но у нас осталась возможность обратиться к нему с помощью **file4**. Это как два человека, использующие одну пластиковую карту и знающие пароль от неё. Не станет одного человека, но карта и пароль то остануться, а значит второй сможет, как и раньше, пользоваться картой  
*Ну это - как понял я. Может и чушь несу, конечно))*
---
### Дать созданным файлам другие, произвольные имена. Создать новую символическую ссылку. Переместить ссылки в другую директорию.
1. Поочерёдно переименовываю **file2** в **copied_file**, **file3** в **soft_file**, **file4** в **hard_file**  
![image](https://user-images.githubusercontent.com/108574612/215751156-eaf79b76-d769-4cb4-bd3d-b25c5255e613.png)
2. Создал символическую ссылку **abs_soft_file** на **copied_file** (в девичестве file2). При создании использовал абсолютный путь, чтобы при переносе в новую директорию, ссылка не стала бесполезной  
![image](https://user-images.githubusercontent.com/108574612/215758327-0ca6927f-60c5-4910-b69b-1c294f936573.png)

3. Создал директорию **new_dir**. Переместил в неё **hard_file**, **abs_soft_file**,  **soft_file** (последний как был бесполезен после удаления file1, так и останется)  
![image](https://user-images.githubusercontent.com/108574612/215759041-23e4effd-7a3b-4983-94e8-2f4c5f6b0f38.png)  
*copied_file не переместил в новую директорию, так как создан он был копированием, а не как ссылка. А в задании сказано именно ссылки переместить. Конечно, если глубже копнуть, то и он окажется ссылкой, наверное. Но не думаю, что в задании это учитывалось*
---
## Спасибо за интересный семинар! :)


