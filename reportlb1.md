## Лабораторная работа 1

### **1. Скачивание Boost**
wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz

Команда для скачивания:

```bash
wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
```
Результат выполнения программы:

```bash
--2026-06-06 23:03:37--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
Распознаётся sourceforge.net (sourceforge.net)… 104.18.13.149, 104.18.12.149, 2606:4700::6812:d95, ...
Подключение к sourceforge.net (sourceforge.net)|104.18.13.149|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/ [переход]
--2026-06-06 23:03:38--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download [переход]
--2026-06-06 23:03:38--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABqJH0a_txZAd-ZjKYTM9QJHlBcAP34EyrdV1wvRD25U4UC85UhMrKQRR3g9nYPJJ0bGeHoegq1u30jznYCm7Yd1cP2Kw%3D%3D&use_mirror=altushost-swe&r= [переход]
--2026-06-06 23:03:39--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABqJH0a_txZAd-ZjKYTM9QJHlBcAP34EyrdV1wvRD25U4UC85UhMrKQRR3g9nYPJJ0bGeHoegq1u30jznYCm7Yd1cP2Kw%3D%3D&use_mirror=altushost-swe&r=
Распознаётся downloads.sourceforge.net (downloads.sourceforge.net)… 104.18.12.149, 104.18.13.149, 2606:4700::6812:d95, ...
Подключение к downloads.sourceforge.net (downloads.sourceforge.net)|104.18.12.149|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://altushost-swe.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1&fid=0b04351a8c20a7ca [переход]
--2026-06-06 23:03:39--  https://altushost-swe.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1&fid=0b04351a8c20a7ca
Распознаётся altushost-swe.dl.sourceforge.net (altushost-swe.dl.sourceforge.net)… 79.142.76.130
Подключение к altushost-swe.dl.sourceforge.net (altushost-swe.dl.sourceforge.net)|79.142.76.130|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 111710205 (107M) [application/x-gzip]
Сохранение в: «boost_1_69_0.tar.gz»

boost_1_69_0.tar.gz 100%[===================>] 106,53M   834KB/s    за 2m 34s  

2026-06-06 23:06:15 (707 KB/s) - «boost_1_69_0.tar.gz» сохранён [111710205/111710205]
```
### **2 Разархивирование**
tar -xvzf boost_1_69_0.tar.gz -C ~/

### **3. Подсчёт количества файлов (без вложенных директорий)**

> Команда :  find ~/boost_1_69_0 -maxdepth 1 -type f | wc -l

    ❯ find ~/boost_1_69_0 -maxdepth 1 -type f | wc -l
    
    16


### **4. Подсчёт количества файлов (включая вложенные директории)**
команда

    find ~/boost_1_69_0 -type f | wc -l
 Результат 

     ❯ find ~/boost_1_69_0 -type f | wc -l
    
    61198
### **5. Подсчёт заголовочных файлов, .cpp и остальных**
#
Команды 

    find ~/boost_1_69_0 -type f -name "*.hpp" | wc -l
    find ~/boost_1_69_0 -type f -name "*.cpp" | wc -l
    find ~/boost_1_69_0 -type f ! -name "*.hpp" ! -name "*.cpp" | wc -l

#
Результат
#

    ❯ find ~/boost_1_69_0 -type f -name "*.hpp" | wc -l && find ~/boost_1_69_0 -type f -name "*.cpp" | wc -l && find ~/boost_1_69_0 -type f ! -name "*.hpp" ! -name "*.cpp" | wc -l
    
    14912
    13774
    32512

#
 
### **6. Поиск пути до файла `any.hpp`**
#
Команды 

    find ~/boost_1_69_0 -type f -name "any.hpp"


#
Результат
#

   

    ❯ find ~/boost_1_69_0 -type f -name "any.hpp"
    
    /home/sabirovatv/boost_1_69_0/boost/type_erasure/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/proto/detail/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/hana/fwd/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/hana/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/fusion/include/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
    /home/sabirovatv/boost_1_69_0/boost/fusion/algorithm/query/any.hpp



#


### **7. Поиск файлов с `boost::asio`**


#
Команды 

    grep -rl "boost::asio" ~/boost_1_69_0


#
Результат
#
 
   -[result](https://raw.githubusercontent.com/sabirovatv/lab1/refs/heads/main/log.txt?token=GHSAT0AAAAAAD62LAJYAJIXQ4OCCHZ6UU4C2RATMRQ)
#

### **8. Компиляция Boost**

# команда

    cd ~/boost_1_69_0  && ./bootstrap.sh && ./b2

# Результат 
[build_output.txt](https://github.com/sabirovatv/lab1/blob/main/build_output.txt)

## 9. Перемещение статических библиотек

# Команда

    mkdir -p ~/boost-libs && find ~/boost_1_69_0/stage/lib -type f -name "*.a" -exec mv {} ~/boost-libs/ \;

# Результат 

Перемещенные статические библиотеки 

## 10. Подсчёт занимаемого пространства каждым файлом

# Команда 

    du -sh ~/boost-libs/*

# Результат

    ❯ du -sh ~/boost-libs/*
    
    4,0K	/home/sabirovatv/boost-libs/libboost_atomic.a
    152K	/home/sabirovatv/boost-libs/libboost_container.a
    24K	/home/sabirovatv/boost-libs/libboost_context.a
    328K	/home/sabirovatv/boost-libs/libboost_contract.a
    152K	/home/sabirovatv/boost-libs/libboost_date_time.a
    236K	/home/sabirovatv/boost-libs/libboost_fiber.a
    416K	/home/sabirovatv/boost-libs/libboost_filesystem.a
    836K	/home/sabirovatv/boost-libs/libboost_graph.a
    472K	/home/sabirovatv/boost-libs/libboost_iostreams.a
    212K	/home/sabirovatv/boost-libs/libboost_prg_exec_monitor.a
    1,6M	/home/sabirovatv/boost-libs/libboost_program_options.a
    80K	/home/sabirovatv/boost-libs/libboost_random.a
    3,2M	/home/sabirovatv/boost-libs/libboost_regex.a
    1,2M	/home/sabirovatv/boost-libs/libboost_serialization.a
    40K	/home/sabirovatv/boost-libs/libboost_stacktrace_addr2line.a
    16K	/home/sabirovatv/boost-libs/libboost_stacktrace_basic.a
    4,0K	/home/sabirovatv/boost-libs/libboost_stacktrace_noop.a
    2,3M	/home/sabirovatv/boost-libs/libboost_unit_test_framework.a
    4,5M	/home/sabirovatv/boost-libs/libboost_wave.a
    788K	/home/sabirovatv/boost-libs/libboost_wserialization.a


## 11. Топ-10 самых тяжёлых файлов

# Команда 

    du -sh ~/boost-libs/* | sort -hr | head 
    -10

# Результат

    ❯ du -sh ~/boost-libs/* | sort -hr | head -10
    
    4,5M	/home/sabirovatv/boost-libs/libboost_wave.a
    3,2M	/home/sabirovatv/boost-libs/libboost_regex.a
    2,3M	/home/sabirovatv/boost-libs/libboost_unit_test_framework.a
    1,6M	/home/sabirovatv/boost-libs/libboost_program_options.a
    1,2M	/home/sabirovatv/boost-libs/libboost_serialization.a
    836K	/home/sabirovatv/boost-libs/libboost_graph.a
    788K	/home/sabirovatv/boost-libs/libboost_wserialization.a
    472K	/home/sabirovatv/boost-libs/libboost_iostreams.a
    416K	/home/sabirovatv/boost-libs/libboost_filesystem.a
    328K	/home/sabirovatv/boost-libs/libboost_contract.a




