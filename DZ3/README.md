## Домашнее задание

Работа с LVM

## 🎯 Задание



  Уменьшить том под / до 8G.

  Выделить том под /home.

  Выделить том под /var - сделать в mirror.

  /home - сделать том для снапшотов.

  Прописать монтирование в fstab. Попробовать с разными опциями и разными файловыми системами (на выбор).

 Работа со снапшотами:

  сгенерить файлы в /home/;

  снять снапшот;

  удалить часть файлов;

  восстановиться со снапшота.


## Процесс уменьшения тома /:

### Создаём LVM-том 8 ГБ на /dev/sdc

pvcreate /dev/sdc
vgcreate vg_root /dev/sdc
lvcreate -n lv_root -L 8G /dev/vg_root

### Форматируем в ext4 и монтируется в /mnt/root

mkfs.ext4 /dev/vg_root/lv_root
mkdir /mnt/root
mount /dev/vg_root/lv_root /mnt/root

### Копируем вся система на новый том

rsync -avxHAX --progress / /mnt/root/

### Примонтируем системные директории

for i in /proc/ /sys/ /dev/ /run/ /boot/; do sudo mount --bind "$i" "/mnt/root/$i"; done
sudo chroot /mnt/root/

### Обновляем загрузчик и initramfs
grub-mkconfig -o /boot/grub/grub.cfg
update-initramfs -u

После перезагрузки система запустится с нового тома нужного объема

Скриншот части выполнения команд

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/1.png)

Проверка

![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/2.png)

 ## Выделяем том под /home.
 
![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/3.png)

 ## Выделяем том под /var - делаем в mirror.

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/4.png)

 ## /home - делаем для снапшотов.

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/5.png)

 ##  Прописываю монтирование в fstab

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/6.png)

 ## Работа с снапшотами

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/7.png)
 
 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/8.png)

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/9.png)

 ![alt text](https://github.com/Eliminir/LIN_PROF/blob/main/DZ3/10.png)
 





