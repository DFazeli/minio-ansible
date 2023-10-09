=========

Repository ini digunakan untuk menginstall `minio` server untuk Linux

Support platform

- Debian
- Ubuntu
- CentOS


Requirements
------------

None

Role Variables
--------------

Ada beberapa variable yang temen-temen bisa gunakan untuk setting docker daemon, diantaranya seperti berikut:

| Variable name                 | Example value     | Description |
| :---                          | :---              | :---        |
| `minio_access_key`            | `-`               | Set user credential for minio server |
| `minio_secret_key`            | `-`               | Set password credential for minio server |
| `minio_volume_bind`           | `/var/lib/minio`  | Set data to store ini minio object storage |
| `minio_ports_api`             | `9000`            | Set port to access api s3 |
| `minio_ports_console`         | `9664`            | Set port to access web console |
| `Disk1`                       | `/dev/sdb`        | Set disk for minio drive |
| `Disk2`                       | `/dev/sdc`        | Set disk for minio drive |


Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

minio-playbook.yaml

```yaml
- hosts: servers
  become: true
  roles:
      - { role: minio-asnible }
```

`ansible-playbook -i hosts.txt minio-playbook.yaml`



