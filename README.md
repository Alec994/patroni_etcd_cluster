# patroni_etcd_cluster
This ansible playbook creates patroni etcd cluster

Для корректной работы playbook необходимо выполнить несколько условий:

1. В файле inventory.ini должны быть указаны корректные группы. В репозитории есть образец этого файла (inventory_example.ini).
2. Необходимо указать правильный путь до директории templates.
3. Также можно настроить директорию для БД в разделе "Create database directory and giving privileges". По умолчанию создаётся директория /data/pg_data с правами 0700 и владельцем postgres:postgres.
4. Все учётные записи создаются с паролем password. Настоятельно рекомендуется настроить собственные пароли в директории templates, в файле patroni_yaml.j2, в разделах:
- user
- authentication
