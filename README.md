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
