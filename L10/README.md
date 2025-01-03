# **Основные задачи**

[Script1](https://github.com/kruasann/MobyDZ/blob/main/L10/scripts/script1)
1. Вам дан файл со следующим содержимым:

   > 2014-10-12 14:22:44 OK 
   >
   > 2014-10-12 16:11:41 OK 
   >
   > 2015-02-11 14:12:31 OK 
   >
   > 2015-05-05 03:17:11 
   >
   > 2020-08-06 12:11:31 
   >
   > 2020-07-07 11:17:51 OK 
   >
   > 2020-05-08 14:15:21

   ![image](https://github.com/user-attachments/assets/931d600d-4026-4fd8-a9cf-94e05410112f)


   Нужно взять и посчитать количество строк с выводом “ОК” в конкретный день.
   
   ![image](https://github.com/user-attachments/assets/20edb1d4-644d-4950-aace-c136802951ef)

   Вывод должен быть примерно таким:

   > 2014-10-12 2 
   >
   > 2015-02-11 1 
   >
   > 2015-05-05 0 
   >
   > 2020-08-06 0 
   >
   > 2020-07-07 1 
   >
   > 2020-05-08 0

   ![image](https://github.com/user-attachments/assets/ad5cb5d0-4f57-476f-baa7-f3609f4ff68b)


2. Заменить существующее расширение в имени файла на заданное (jpg -> png) [Script2](https://github.com/kruasann/MobyDZ/blob/main/L10/scripts/script2)

   Исходное имя файла и новое расширение передаются скрипту в качестве параметров.

   ![image](https://github.com/user-attachments/assets/2b0d4b2c-a177-4f1c-952e-825ccb8b942f)

   ![image](https://github.com/user-attachments/assets/f6766d90-8406-4a38-93a9-630e1ce3ca42)
   
3. Создать скрипт, который записывает текущие процессы, открытые порты, список пользователей системы, локальный IP и свободное место на диске в файл с именем output.txt. Если такой файл уже существует, записать в файл с именем output_new.txt [Script3](https://github.com/kruasann/MobyDZ/blob/main/L10/scripts/script3)

   ![image](https://github.com/user-attachments/assets/efebba82-2ab1-42cd-b709-cd6e750751dd)

   ![image](https://github.com/user-attachments/assets/857286b6-7bc7-4342-a27f-00d07b012d23)

# **Дополнительная задача** [Script4](https://github.com/kruasann/MobyDZ/blob/main/L10/scripts/script4)

4. Организация таймера — периодическая выдача на stdout сообщения о том, сколько времени прошло после запуска таймера (т.е. скрипта) и сколько осталось до конца работы.

   Параметры таймера передать при запуске скрипта через параметры. 

   Основные средства: структуры while или until, средства для организации счетчика.

   ![image](https://github.com/user-attachments/assets/9ffa39e5-a7d9-42aa-af34-065fa10cc82e)

   ![image](https://github.com/user-attachments/assets/161c8993-4fac-45bd-ac67-abde3543d618)
