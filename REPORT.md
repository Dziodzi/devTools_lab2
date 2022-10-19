### 1. Мною был запущен локальный веб-визуализатор репозитория и в нём отображалось нормальное описание репозитория; ###

### 2. Перенесены все коммиты, находившиеся в ветке ci, в ветку master с объединением всех коммитов в один и изменением сообщения таким образом, чтобы оно полностью описывало все вносимые изменения. Удалена ветка ci; ###

<a href="https://ibb.co/HD7W69x"><img src="https://i.ibb.co/XZXh1G3/photo-2022-10-19-11-12-00.jpg" alt="photo-2022-10-19-11-12-00" border="0"></a>

### 3. Найден последний коммит и создана ветка old-master; ###

<a href="https://ibb.co/jRvDGTS"><img src="https://i.ibb.co/WtWfF6L/photo-2022-10-19-11-15-43.jpg" alt="photo-2022-10-19-11-15-43" border="0"></a>

### 4. Определён коммит, в котором строчка 32 файла prisma/seed.ts изменялась в последний раз, и его дата; ###

*git blame prisma/seed.ts*

<a href="https://ibb.co/KFnZSbd"><img src="https://i.ibb.co/t8RfFQg/t4.jpg" alt="t4" border="0"></a>

### 5. Найден коммит, в котором проявился регресс; ###

*npm install --save-dev jest* <br />
*git checkout master* <br />
*git bisect start* <br />
*git bisect bad* <br />

<a href="https://imgbb.com/"><img src="https://i.ibb.co/Jshb8Yc/2022-10-19-130628377.png" alt="2022-10-19-130628377" border="0"></a>

### 6. Удалён .env из всех коммитов и добавлен в .gitignore; ###

*git filter-branch --tree-filter "rm -f .env" -- --all* <br />
*echo .env >> .gitignore* <br />

<a href="https://ibb.co/VMdVT9v"><img src="https://i.ibb.co/TPZct2H/2022-10-19-131425092.png" alt="2022-10-19-131425092" border="0"></a>

### 7. Автором коммитов в ветке feature стал я. Неприятно, но терпимо; ###

<a href="https://ibb.co/KzzZJS6"><img src="https://i.ibb.co/vvv5SR1/2022-10-19-132453362.png" alt="2022-10-19-132453362" border="0"></a>