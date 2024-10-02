# Домашнее задание к занятию 4 «Работа с roles» Шарапат Виктоп

## Подготовка к выполнению

1. * Необязательно. Познакомьтесь с [LightHouse](https://youtu.be/ymlrNlaHzIY?t=929).
2. Создайте два пустых публичных репозитория в любом своём проекте: vector-role и lighthouse-role.
3. Добавьте публичную часть своего ключа к своему профилю на GitHub.

## Основная часть

Ваша цель — разбить ваш playbook на отдельные roles. 

Задача — сделать roles для ClickHouse, Vector и LightHouse и написать playbook для использования этих ролей. 

Ожидаемый результат — существуют три ваших репозитория: два с roles и один с playbook.

**Что нужно сделать**

1. Создайте в старой версии playbook файл `requirements.yml` и заполните его содержимым:

   ```yaml
   ---
     - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
       scm: git
       version: "1.13"
       name: clickhouse 
   ```

2. При помощи `ansible-galaxy` скачайте себе эту роль.
3. Создайте новый каталог с ролью при помощи `ansible-galaxy role init vector-role`.
4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`. 
5. Перенести нужные шаблоны конфигов в `templates`.
6. Опишите в `README.md` обе роли и их параметры. Пример качественной документации ansible role [по ссылке](https://github.com/cloudalchemy/ansible-prometheus).
7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.
8. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в `requirements.yml` в playbook.
9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения `roles` с `tasks`.
10. Выложите playbook в репозиторий.
11. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

---

# Решение

*данные дейстия анолочны для каждой роли*

* настроил публичную часть своего ключа к своему профилю на GitHub.
* создал три пустых публичных репозитория:
   - vector-role
   - lighthouse-role
   - clickhouse-role

## ClickHouse 

*создал роль*

   - ansible-galaxy role init clickhouse
   
# стркутура роли:
    
defaults - переменные для роли

files - файлы, для установки роли

handlers - как и в плейбуке, отдельный файлы

meta - автор, описание роли, тип лицензии, версия ансибел, ОС, теги, зависимости

tasks - ямл файлы, таски

templates -шаблоны

tests - тестовый плейбуке 

vars  -переменные, которые пользователь не меняет через плейбуке (defaults)

README.md - описание

**Перенес в соответствующие папки блоки с основного плейбука, заполнил необходимые файлы информацией.**

*Выполнил следующие команды для пуша в Gityub:* 

* Перейдите в директорию вашей роли
* git init
* git add .
* git commit -m "clickhouse-role"
* git remote set-url origin git@github.com:sharvik22/clickhouse-role.git
* git push -u origin main
* git tag -a v1.0.0 -m "Release v1.0.0"
* git push origin v1.0.0

![image](https://github.com/user-attachments/assets/0e5215c8-bc99-4664-8aef-5c508d2c30c8)

### https://github.com/sharvik22/clickhouse-role.git

*Выполнил следующие команды для загрузки роли:* 


* перейти в директорию плейбука
* скопировать ссылку ssh с Github
* в директории с плейбуком создать файл requirements.yml

---
  - name: clickhouse-role
    src: git@github.com:sharvik22/clickhouse-role.git
    scm: git
    version: "v1.0.0"  

* скачал роль с Github
   
ansible-galaxy install -r requirements.yml -p roles




### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---




