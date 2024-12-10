Домашнее задание к занятию 4 «Работа с roles»
=========

Этот плейбук установит `Clickhouse`, `Vector` и `Lighthouse`

используются три роли :

```yaml
  - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.13"
    name: clickhouse 
```

2. vector

```yaml
  - name: vector
    src: git@github.com:barmaq/ansible-vector-role.git
    scm: git
```

3. lighthouse
   
```yaml
  - src: git@github.com:barmaq/ansible-lighthouse-role.git
    scm: git
    name: lighthouse
```


роль `Clickhouse` установится на любое семейство OS
роли `Vector` и `Lighthouse` установятся на семейство OS `debian`  


Переменные
--------------

| Переменная  | Назначение  |
|:---|:---|
| `vector_version` | версия `Vector` |

подробное описание перпеменных для Clickhouse  
https://github.com/AlexeySetevoi/ansible-clickhouse/blob/master/README.md


Playbook
-------
Playbook состоит из 3 `play`.

"Install clickhouse" используется на группу хостов "Clickhouse" и устанавливает `Clickhouse`

"Install Vector" используется на группу хостов "Vector" и устанавливает `Vector`

"Install lighthouse" используется на группу хостов "lighthouse" и устанавливает `Nginx` и `lighthouse`



License
-------

MIT

Информация о Авторе
------------------

Victor SHumskiy
