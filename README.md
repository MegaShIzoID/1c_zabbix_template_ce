[![CodeFactor](https://www.codefactor.io/repository/github/slothfk/1c_zabbix_template_ce/badge)](https://www.codefactor.io/repository/github/slothfk/1c_zabbix_template_ce)

# 1c_zabbix_template_ce (Community Edition)
Шаблон (конфигурационные файлы агента и вспомогательные скрипты) для мониторинга с помощью Zabbix (версии 4.4) серверов 1С Предприятия, работающих как под управлением операционной системы GNU/Linux так и под MS Windows.
Позволяет собирать информацию одновременно с разных сервисов **RAS** (для чего в макросе **{$RAS_PORTS}** необходимо указывать порты, используемых **RAS** через запятую)

## Основная идея проекта
* Расследование инцидентов, возникающих в работе сервера 1С Предприятия, с минимальной задержкой от момента их возникновения
* Хранение минимального объема информации, нобходимого для расследования

## Выбранная архитектура
Шаблон разбит на несколько составляющих по функциональному назначению:
* Шаблон для мониторинга [рабочего сервера](./docs/work_server.md) 1С Предприятия
* Шаблон для мониторинга [сервера лицензирования](./docs/license_server.md)
* Шаблон для мониторинга [центрального сервера](./docs/central_server.md)

Неявно подразумевается, что на сервере (объекте мониторинга) запущенна **только одна служба сервера 1С Предприятия** (агент сервера 1С Предприятия)

## Установка и обновление
Описание процесса установки можно найти [здесь](./docs/install.md). Специфика использования скриптов на платформе MS Windows описана [здесь](./docs/windows.md)

Т.к. шаблон находится в состоянии активной разработки (добавляются новые функции, корректируется имеющийся функционал), то может возникнуть ситуация, когда на работающей системе необходимо привести уже развернутый шаблон к актуальному состоянию. К сожалению, на текущий момент универсальной инструкции, позволяющей перейти к актуальной версии, и при этом не потерять накопленные данные, **нет**!

## Статьи о данном шаблоне (с картинками)
* [Мониторинг количества использованных программных лицензий, выданных выделенным сервером лицензирования](https://infostart.ru/public/1157013/)
* [Использование Zabbix для сбора информации о серверных вызовах и управляемых блокировках с сервера 1С Предприятия, работающего на платформе GNU/Linux](https://infostart.ru/public/1120500/)
* [Мониторинг количества использованных клиентских лицензий, выданных сервером 1С Предприятия, работающим на платформе GNU/Linux](https://infostart.ru/public/1114020/)
