
1. Изучите Linux Kernel Defense Map и ознакомьтесь с основными механизмами защиты ядра Linux.

  ![image](https://github.com/a13xp0p0v/linux-kernel-defence-map/blob/master/linux-kernel-defence-map.svg)

2. Используйте инструмент kernel-hardening-checker для анализа текущего состояния безопасности вашей системы.
   Установим инструмент по гайду из репозитория
   
   ![image](https://github.com/user-attachments/assets/5932fb46-ec13-40e7-9c3d-13d9ffbb5d22)
   
3. Выполните следующие шаги:
   * Запустите kernel-hardening-checker и проанализируйте полученные результаты.

   ![image](https://github.com/user-attachments/assets/78c44351-193a-460f-b8b0-16ba44d36fb4)

   Проверка конфигурации ядра показала, что большинство параметров защиты настроены корректно, но есть несколько недочетов: некоторые параметры безопасности ядра и защиты от уязвимостей (например, Spectre, Meltdown) не активированы. Рекомендуется включить недостающие параметры, улучшить защиту от атак на стек и настройки для повышения безопасности системы
   
   [+] Config check is finished: 'OK' - 149 / 'FAIL' - 151

   * Опишите найденные уязвимости и проблемы в безопасности (не обязательно прям все, штучки 2-3)
     * Spectre (Variant 2) Уязвимость использует методы спекулятивного выполнения для утечки данных через кэш-память. Атакующий может заставить процессор выполнить нежелательные вычисления, что позволяет извлечь секретные данные, например, из другого процесса
      
     ![image](https://github.com/user-attachments/assets/bf521321-52df-45fd-85f4-6266bd8a8148)
   
     ![image](https://github.com/user-attachments/assets/21e64e22-26af-4019-873e-cc22b39bda5a)
     
     ![image](https://github.com/user-attachments/assets/8e66f024-20b1-48ab-83f9-9ae48aae41f5)

     * Уязвимость Meltdown позволяет атакующему получить доступ к защищенной памяти, нарушая изоляцию процессов. Она влияет на процессоры Intel и может быть использована для получения доступа к ядру системы
     
     ![image](https://github.com/user-attachments/assets/6ed0b94d-1b74-4aaa-811c-d9099420de36)

     ![image](https://github.com/user-attachments/assets/ca9399f5-20c3-4f9c-8ae2-4673985685c2)
     
     ![image](https://github.com/user-attachments/assets/8ac18876-b25b-459f-b0a7-70cf7cf8a822)

   * Примите конкретные меры по усилению безопасности для каждой выявленной уязвимости.


4. На основе анализа и предложений, разработайте план действий по улучшению безопасности ядра Linux на вашей системе p.s. это может быть нечто автоматизированное.

   [Примерный скрипт для устранения вышеуказанных уязвимостей](https://github.com/kruasann/MobyDZ/edit/main/L5/script.txt)

   ![image](https://github.com/user-attachments/assets/9e18ebfd-9a62-4f34-b8d5-0a262e68aa6a)

