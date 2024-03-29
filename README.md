# Ansible 入门指南

## 学习笔记

- [Ansible 入门指南 - 安装及 Ad-Hoc 命令使用](https://www.cnblogs.com/michael-xiang/p/10426159.html)
- [Ansible 入门指南 - ansible-playbook 命令](https://www.cnblogs.com/michael-xiang/p/10461518.html)
- [Ansible 入门指南 - 常用模块](https://www.cnblogs.com/michael-xiang/p/10461501.html)
- [Ansible 入门指南 - 学习总结](https://www.cnblogs.com/michael-xiang/p/10462749.html)

## ad-hoc

该目录是初步学习 ansible 建立的文件夹，用来熟悉 `ansible.cfg`/`hosts`等基础概念的。

例如这样的命令：

```shell
ansible all -m shell -a "cat /var/www/html/index.html"
```

## playbook-simple

该目录是学习 playbook 相关模块时的归档文件，里边没有按照推荐的目录规范建立，可以用如下的命令运行里边 playbook 脚本：

```shell
cd playbook-simple
ansible-playbook loop_learn.yml
```

## ansible-own

该目录存放一下自己写的一些 playbook

### mysql

该目录下放了自己安装 mysql 的脚本，运行命令：

```
cd ansible-own/mysql
ansible-playbook site.yml --list-hosts
ansible-playbook site.yml --list-tasks
ansible-playbook site.yml
```

`mysql_master_remove` 谨慎执行该 task，原来机器上有 MySQL 的话，可能会造成数据丢失。

脚本会自动安装 mysql-5.7，并将数据存储路径设置为 `/data/mysql`的目录下。