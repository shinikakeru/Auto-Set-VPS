# Запуск

<span style="font-size: 24px;">1. Зайти на сервер по ssh от имени **root**</span>
<span style="font-size: 24px;">2. Ввести команду</span>
<span style="font-size: 24px;">3. Все выполнится автоматически</span>

```bash

wget -qO- "https://raw.githubusercontent.com/shinikakeru/Auto-Set-VPS/main/vps.sh?cache=$(date +%s)" > setup.sh \&\& chmod +x setup.sh \&\& sudo ./setup.sh ; rm -f setup.sh

```

## Что делает скрипт

<span style="font-size: 24px;">1. Меняет порт на 1024 для ssh в **/etc/ssh/sshd\_config**</span>
<span style="font-size: 24px;">2. Добавляет SSH ключ в **/root/.ssh/authorized\_keys** **(опционально)**</span>
<span style="font-size: 24px;">3. Скрывает баннеры **PrintMotd** и **PrintLastLog**, которые идут по умолчанию в **/etc/ssh/sshd\_config**</span>
<span style="font-size: 24px;">4. Создает свой баннер</span>
<span style="font-size: 24px;">5. Автоматически настраивает фаервол, оставляет открытым \*\*только порт для ssh\*\*</span>
<span style="font-size: 24px;">6. Перезапускает службы</span>
<span style="font-size: 24px;">7. Чистит файлы за собой</span>
