# bot_installation
Руководство по установке для бота-выдающего .conf файлы

Файлы: 
------
1. env - Виртуальное окружение
2. main.py - Код телеграм бота(Запускать бота из этого файла)
3. keyboard.py - Клавиатура бота
4. find_files.py - Код поиска .conf файлов пользователя
5. logs.txt - Логи
6. config.txt - Сюда вводить API токен бота
7. csv_checker.py - Просматривает csv файл на наличие пользователя

Установка:
----------
1. Заходим на сервер
2. Заходим в папку где лежат папки, внутри которых peer_{username}
```
cd путь-к-папке
```
3. В той же директории создаем папку в которой будем размещать бота
```
mkdir -p Название-папки
```
4. Закидываем .rar архив и распаковываем его
5. Меняем config.txt на токен вашего бота. 
6. Проверяем терминал на наличие python3-pip. Если его нет устанавливаем командами:
```
sudo apt update
sudo apt -y upgrade
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
sudo apt install -y python3-pip
```
7. Устанавливаем и активируем виртуальное окружение:
```
sudo apt install -y python3-venv
python3 -m venv env
source env/bin/activate
```
8. Устанавливаем python библиотеку aiogram:
```
pip3 install aiogram
```
9. Устанавливаем утилиту screen:
```
apt install screen
screen
```
  Когда появилось окно нажимаем пробел.

10. Запускаем бота:
```
python main.py
```
ГОТОВО!
=======
### P.S.
Если захотели отключить бота.

1. Если у вас запущено больше чем одна screen - сессия:
  ```
  screen -ls
  ```
  Выбираем нужный нам screen, и присоединяемся к нему. Например:
  ```
  screen -x 2762.pts-0.debian
  ```
  Прожимаем Ctrl — a и вводим команду 
  ```
  :quit
  ```
2. Если сессия одна:
  ```
  screen –x
  ```
  Прожимаем Ctrl — a и вводим команду 
  ```
  :quit
  ```
