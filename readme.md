# How to start

```sh
$ ansible-playbook playbook.yml -i inventory --private-key <key>
```

- run only one task
use ``tags``

```sh
- name: Copy NGINX Config File
    copy: src=nginx.conf dest=/etc/nginx/sites-available/default
    tags: copy <- here
...

$ ansible-playbook playbook/playbook.yml -i inventory --private-key ~/project/work/ditto/key/private --tags tag
```