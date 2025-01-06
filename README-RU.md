<img src="src/App GitHub Header.png" width="100%"/>

# Salt Player - музыкальный плеер, выбранный сотнями тысяч пользователей

Select language: [中文](https://github.com/Moriafly/SaltPlayerSource/blob/main/README.md)，[Indonesia](https://github.com/Moriafly/SaltPlayerSource/tree/main/README-ID.md)

Salt Player - это локальный музыкальный плеер. Этот репозиторий используется для публикации новых версий, сбора отзывов и объявлений.

## Каналы загрузки

### Android

Salt Player *для Android* требует Android 6.0 и выше, поддерживает архитектуры arm-v8a и armeabi-v7a

| Канал | Релиз | Описание | ⚠️ Примечание |
|:--|:--|:--|:--|
| Moriafly | 1. [Github Release](https://github.com/Moriafly/SaltPlayerSource/releases) <br> 2. [CoolApk](https://www.coolapk.com/apk/284064) | Стандартная версия | CoolApk предоставляет только версию для arm64-v8a |
| Google Play | [Google Play](https://play.google.com/store/apps/details?id=com.salt.music) | Версия для Google Play | 1. Динамическая доставка для arm64-v8a/armeabi-v7a <br> 2. Версия Google Play подписана Google и **несовместима** со стандартной версией <br> 3. Может использовать специальные стабильные версии или специальные сборки, отличающиеся от стандартной версии |
| Official | 1. OPPO Store <br> 2. [Honor Store](https://appmarket-h5.cloud.honor.com/h5/share/latest/index.html?shareId=1842107500028387328&shareTo=copyLink) <br> 3. [Xiaomi Store](http://app.xiaomi.com/detail/1610743) <br> 4. [Huawei AppGallery](https://url.cloud.huawei.com/sztUvRf1XW) <br> *Порядок указан по дате публикации, ссылка на OPPO Store пока недоступна* | Версии для китайских магазинов | 1. Только для arm64-v8a <br> 2. Поддержка только для материкового Китая <br> 3. Может использовать специальные стабильные версии или специальные сборки <br> 4. Из-за проверок и других причин, скорость обновления и номера версий могут различаться в разных магазинах |

Примечание: Пожалуйста, загружайте приложение только из официальных каналов и не используйте установочные файлы из неизвестных источников

#### Правила именования версий (файлов)

Например, имя APK файла 10.5.0.2-release-2024091902-moriafly-arm64-v8a означает:

| Текст | Обозначение | Описание |
|:--|:--|:--|
| 10.5.0.2 | Версия | 10 - основная версия, 5 - второстепенная версия, 0 - патч，2 - аварийный патч (Если патчей не было, то обычно 0 опускается, например просто 10.4.4) |
| release | Тип версии | 1. release - стабильная версия, beta - публичная бета, alpha - тестовая версия в которой могут быть серьезные ошибки <br> 2. release обычно опускается, alpha может быть публичной, но менее стабильной <br> 3. Стабильность: release > beta > alpha (субъективно) |
| 2024091902 | Код версии | Код версии Salt Player *для Android* имеет значение: 2024091902 означает вторую сборку 19 сентября 2024 года |
| moriafly | Код канала | См. таблицу каналов |
| arm64-v8a | Архитектура | См. таблицу каналов |

### Windows

<img src="src/spw.png" height="128px"/>

Подробнее: [SPW](https://github.com/Moriafly/SPW)

## Библиотеки с открытым исходным кодом

[Salt UI](https://github.com/Moriafly/SaltUI)

## Локализация

Подробности в [документации](https://github.com/Moriafly/SaltPlayerSource/tree/main/translations)

## Системная интеграция

| Система | Функция | Статус | Примечание |
|:--|:--|:--|:--|
| Xiaomi MIUI/Hyper OS | Xiaomi Smart Cast | 🟢 Поддерживается | 1. Требуется MIUI 12 и выше, нажмите кнопку в правом верхнем углу экрана воспроизведения <br> 2. Функция основана на системных компонентах трансляции Xiaomi, проверьте, не отключены ли они |
| | CarWith | 🟢 Поддерживается | Поддержка добавлена в CarWith 3.3.6 от 26 декабря 2024, спасибо Xiaomi за поддержку |
| | Внешний экран (например Mix Flip) | 🟢 Поддерживается | |
| | Виджеты MIUI/Hyper OS | 🟠 В разработке | Ожидает разработки |
| Huawei HarmonyOS | Центр управления музыкой | 🔴 Не поддерживается | Документация по портированию под API не найдена |
| vivo OriginOS/Funtouch OS | Jovi InCar | 🟢 Поддерживается | 1. Поддержка Salt Player добавлена в vivo Smart Car V4.0.7.3 от 29 августа 2024, спасибо пользователям за отзывы и vivo за поддержку <br> 2. Бета-версия, пока не поддерживает отображение текста в Jovi InCar (метод адаптации неизвестен), можно использовать эмуляцию текста через Bluetooth |
| | Hi-Fi | 🔵 Вручную | 1. Добавьте через adb командой `settings put global game_support_hifi_list com.salt.music` <br> 2. После добавления включите в Настройки > Звук и вибрация > Hi-Fi <br> 3. Поддержка Hi-Fi зависит от устройства, проверьте на официальном сайте vivo |
| | Atomic Island | 🔴 Не поддерживается | Ничего не известно, документация по портированию под API не найдена <br> [#749](https://github.com/Moriafly/SaltPlayerSource/issues/749) |
| OPPO ColorOS | Fluid Cloud | 🟢 Поддерживается | Постепенное тестирование с 4 ноября 2024, спасибо OPPO за поддержку |
| Meizu Flyme | Текст в строке состояния | 🟢 Поддерживается | |
| | Dynamic Island | 🔴 Не поддерживается | Ничего не известно, документация по портированию под API не найдена |

## Прекращенные функции

| Функция | Дата прекращения | Примечание |
|:--|:--|:--|
| DSD аудио (.dsf/.dff) | 2024 | Считается устаревшим форматом, рекомендуется перейти на FLAC <br> Подробнее в [Salt Player прекращает поддержку формата DSD](https://github.com/Moriafly/SaltPlayerSource/blob/main/articles/240902_Deprecated_DSD.md) [(Перевод)](https://github.com/Moriafly/SaltPlayerSource/blob/main/articles/241123_Deprecated_DSD_russian_translate.md) |

## Участники репозитория

<a href="https://github.com/Moriafly/SaltPlayerSource/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=Moriafly/SaltPlayerSource&columns=12" />
</a>

## Юридическая информация

**Android** является товарным знаком Google LLC

**Android Robot** создан или модифицирован на основе работы, созданной и распространяемой Google, и используется в соответствии с условиями [Creative Commons](https://creativecommons.org/licenses/by/3.0/) Attribution 3.0

**Salt Player** и **糖醋音乐** являются зарегистрированными товарными знаками Xunxun Technology (Shanghai) Co., Ltd. в Китайской Народной Республике

Дополнительную юридическую информацию можно найти в приложении и на соответствующих веб-сайтах
