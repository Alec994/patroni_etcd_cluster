# patroni_etcd_cluster
This ansible playbook creates patroni etcd cluster

Для того чтобы playbook отрабатывал правильно, необходимо выполнить несколько условии.
1. Необходимо в файле inventory.ini прописать правильные группы, в репозиторий есть образец.
2. Необходимо указать правильный путь до директории templates.
3. Также можно настривать директорию для БД в разделе "Create database directory and giving privileges" по умолчанию создается директория /data/pg_data с правами 0700 postgres:postgres 
4. Все учетки создаются с паролем password, также можно даже нужно сконфигурировать пароли в директории templates в файле patroni_yaml.j2 разделах:
- user
- authentication
