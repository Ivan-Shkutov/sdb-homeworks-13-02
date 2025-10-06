## Домашнее задание «Защита хоста»

## Шкутов Иван Владимирович


### Задание 1

Установите eCryptfs.

Добавьте пользователя cryptouser.

Зашифруйте домашний каталог пользователя с помощью eCryptfs.

В качестве ответа пришлите снимки экрана домашнего каталога пользователя с исходными и зашифрованными данными.

### Решение:

sudo apt update

sudo apt install ecryptfs-utils

sudo adduser cryptouser

sudo ecryptfs-migrate-home -u cryptouser (настройка шифрования домашнего каталога, выполнить инициализацию под создаваемым пользователем cryptouser)

sudo passwd cryptouser

su - cryptouser (зашифрованные данные будут храниться в /home/.cryptouser или /home/.ecryptfs/cryptouser в зашифрованном виде)

ecryptfs-unwrap-passphrase (принимает файл и пароль пользователя, возвращая mount passphrase. Полученный mount passphrase нужен для ручного монтирования зашифрованного каталога или для восстановления доступа, если автоматический монтирование не работает.)

![1](https://github.com/Ivan-Shkutov/sdb-homeworks-13-02/blob/main/1.png)

![2](https://github.com/Ivan-Shkutov/sdb-homeworks-13-02/blob/main/2.png)

![3](https://github.com/Ivan-Shkutov/sdb-homeworks-13-02/blob/main/3.png)



### Задание 2

Установите поддержку LUKS.

Создайте небольшой раздел, например, 100 Мб.

Зашифруйте созданный раздел с помощью LUKS.

В качестве ответа пришлите снимки экрана с поэтапным выполнением задания.

### Решение:






