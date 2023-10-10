# ЛР 2. Нестандартные операции при работе с Git

## Цель работы

Получение навыков продвинутой работы с системой контроля версий Git и изучение механизмов его работы на глубоком уровне.

## Описание работы

Вам дан архив с Git-репозиторием, содержащим проект на TypeScript. Необходимо скачать его и выполнить задания, приведённые ниже, в порядке следования. Для запуска проекта вам потребуется Node.js и локальная база данных PostgreSQL (лучше в Docker-контейнере). Для заполнения БД данными используйте команду `npx ts-node prisma/seed.ts`. Чуть более подробный гайд по поднятию есть тут: [Гайд по поднятию Postgres в Docker](https://www.notion.so/Postgres-Docker-7644d9b350944c07aef83dadee024732?pvs=21).

[mobile-dev-backend.zip](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e211003c-ad31-4ae9-b0bc-872f9983fb7f/mobile-dev-backend.zip)

1. Запустите локальный веб-визуализатор репозитория и сделайте так, чтобы в нём отображалось нормальное описание репозитория.
2. Перенесите все коммиты, находящиеся в ветке `ci`, в ветку `master` с объединением всех коммитов в один и изменением сообщения таким образом, чтобы оно полностью описывало все вносимые изменения. Удалите ветку `ci`.
3. В репозитории есть несколько альтернативных историй проекта, недоступных из текущей версии графа **и не связанных с ней**. Найдите последний коммит любой из версий и создайте на нём ветку `old-master`.
4. Определите коммит, в котором строчка 32 файла `prisma/seed.ts` изменялась в последний раз, и его дату.
5. В проекте существует регресс, на который имеется тест, запускающийся по команде `npm run test`. Найдите коммит, в котором проявился регресс.
6. В репозитории существует файл `.env`, содержащий конфиденциальную информацию. Удалите его из всех коммитов, где он присутствует, и добавьте в `.gitignore`.
7. Сделайте так, чтобы автором коммитов в ветке `feature` были Вы. Для этого укажите в изменяемых коммитах почту, привязанную к GitHub, и своё ФИО.
8. Включите запоминание разрешений конфликтов. Влейте ветку `feature` в `master`, разрешив конфликт при слиянии. Откатите слияние, внесите изменение в файл `README.md` и снова влейте ветку `feature` в `master` без ручного разрешения конфликта.
9. Проверьте целостность репозитория и убедитесь, что с ним всё в порядке. При наличии ошибок исправьте их.
10. Проверьте размер репозитория (папки `.git`) и добейтесь уменьшения его размера.
11. В новой ветке `report` создайте файл `REPORT.md` с указанием использованных для выполнения предыдущих пунктов команд и скриншотов результатов работы (поместите их в папку `/docs`). После внесения всей информации сделайте несколько коммитов, каждый из которых будет содержать только те изменения файла `REPORT.md`, которые касаются отдельно взятого пункта (первый коммит добавит команды для первого пункта и соответствующие скриншоты, второй коммит — для второго и т.д.). Отдельным коммитом добавьте команды, которые использовались для поэтапной фиксации файла `REPORT.md`. Загрузите **приватный** репозиторий на GitHub, дайте доступ своему практику и создайте PR для слияния ветки `report` с добавлением ревьюера.
