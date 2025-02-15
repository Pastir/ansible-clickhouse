Role Name
=========
pastir.clickhouse

Role Variables
--------------
### Default value of preset variables:

```
__clickhouse_supported: true
__clickhouse_version: "latest"
__clickhouse_repo: "deb https://packages.clickhouse.com/deb stable main"
__clickhouse_repo_keyserver: keyserver.ubuntu.com
__clickhouse_repo_key: 8919F6BD2B48D754
__clickhouse_packages:
  - clickhouse-common-static
  - clickhouse-server
  - clickhouse-client
 
__clickhouse_uninstall: false
```


Example Playbook
----------------
 ```
 - name: install clickhouse
   hosts: ch_host
   vars:
     clickhouse_version: 24.8.4.13
       
   roles:
     - role: pastir.clickhouse
 ```