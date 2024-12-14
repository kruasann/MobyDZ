# Задание №1


1. Вам необходимо создать 3 группы:

   
   1. it
   2. sales
   3. company
2. Дополнительно создайте директории

   
   1. `/company`
   2. `/company/it`
   3. `/company/sales`
   4. `/company/shared`
3. Теперь создайте пользователей
   * ituser1
   * ituser2
   * itadmin
   * suser1
   * suser2
   * sadmin Так же необходимо выполнить следующие условия:

* У всех юзеров основная группа - company
* У пользователей it\*
  * Оболочка - bash
  * Дополнительная группа - it
  * Домашняя директория внутри - `/company/it`
  * Содержимое директории /company/it должны видеть только root и участники группы it
* У пользователей s\*
  * Оболочка - sh
  * Дополнительная группа - sales
  * Домашняя директория - `/company/sales`
  * Содержимое директории `/company/sales` должны видеть только root и участники группы sales


4. Все пользователи должны видеть содержимое директории `/company/shared` При этом каждый пользователь лично должен внутри директории `/company/shared` создать файл со своим логином.


***

# Задание №2


1. Создайте группы:

   
   1. academy
   2. teachers
   3. students
   4. staff
2. Создайте для них соответствующие директории
3. Создайте пользователей:

   
   1. student
   2. teacher
4. У всех пользователей должны быть домашние директории в соответствующих директориях (например: `/academy/students/student`)
5. Только пользователи групп должны иметь доступ на соответствующие директории (`/academy/students`).
6. Сделайте так, чтобы у группы staff был доступ во все указанные ранее директории
7. Создайте расшаренную директорию `/academy/secret`, внутри которой пользователи групп teachers и staff смогут создавать файлы, но не смогут удалять чужие файлы, так же создайте файл top_secret который не сможет удалить даже root пользователь. У пользователей группы students не должно быть доступа.

   
   1. Создайте «программу» spy, с помощью которой студенты смогут смотреть содержимое директории `/academy/secret` (задание со звездочкой, к выполнению не обязательно)
8. С помощью sudo разрешите пользователям группы students от имени группы teachers удалять файлы внутри `/academy/secret`
9. Создайте файл от учителя внутри директории `/academy/secret`, найдите имя файла с помощью spy от имени студента и удалите файл с помощью sudo от имени студента.


***

# Задание №3


1. Создать директорию `/home/company`.
2. Внутри этой директории нужно создать директории:

   
   1. homedirs
   2. sales
   3. marketing
   4. shared.
3. Создать группы:

   
   1. company
   2. sales
   3. marketing,
4. Создайте пользователей:

   
   1. mike

      
      1. Основная группа - sales
      2. Дополнительная группа - company
   2. john

      
      1. Основная группа - marketing
      2. Дополнительная - company
5. У пользователей домашние директории должны находиться в директории `/home/company/homedirs`. Директории `/home/company/sales` и `/home/company/marketing` должны принадлежать соответствующим группам.
6. У пользователя и группы должны быть все права на директорию.
7. Директория `shared` должна быть расшаренной, её группа должна быть company, и чтобы все новые файлы в этой директории принадлежали группе company.


***

# Задание №4


1. Создайте 3 группы и директории внутри `/data` – marketing, sales и it и
2. Создайте 4 пользователя

   
   1. user.marketing
   2. user.sales
   3. admin
   4. backup.
3. Владельцем директорий должны быть соответствующие пользователи – `user.marketing` владеет директорией `/data/marketing` и т.д.
4. Группы директорий должны соответствовать названиям.
5. У остальных пользователей не должно быть доступа к директориям.
6. Пользователь admin должен иметь полный доступ ко всем директориям,
7. Пользователь backup должен иметь доступ только на чтение.


***

# Задание №5


1. Создайте директорию `/company`, чтобы владельцем был root, а группой - company
2. У владельца и группы должны быть все права, у остальных никаких.
3. Пользователи не должны иметь возможность удалять чужие файлы в этой директории, а все файлы, созданные в этой директории, должны иметь группу company.

---

# Задание №6 (ACL)


1. Создайте в домашнем каталоге новый файл `testfile.txt`. Используйте команду `setfacl` для установки расширенных прав доступа к этому файлу. Например, предоставьте пользователю `john` право на чтение этого файла.
2. Проверьте установленные права с помощью команды `getfacl testfile.txt`
3. Создайте новую директорию `testdir` и установите для нее ACL, который будет наследоваться всеми создаваемыми внутри файлами и поддиректориями. Например, предоставьте группе `developers` права на чтение, запись и исполнение для этой директории и всех ее содержимого
4. Создайте внутри `testdir` файл и директорию, чтобы проверить наследование прав.
5. Измените права доступа для пользователя `john` на файле `testfile.txt`, предоставив ему также право на запись. Затем удалите все ACL с этого файла и проверьте результаты с помощью команды `getfacl`.
6. Изучите, как работают маски в ACL и как они влияют на эффективные права доступа. Попробуйте установить различные комбинации прав и масок для файла и директории, чтобы увидеть, как это отражается на доступе к ним различных пользователей и групп.
