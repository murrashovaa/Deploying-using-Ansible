# Отчет по практической работе 5. Оркестрация узлов в Ansible

## На целевой виртуальной машине обеспечить развертывание конфигурации из внешнего репозитория с помощью инструмента ansible-pull.

## 1. Подготовка

```bash
murashovava@node01:~$ sudo mkdir -p /var/opt/ansible
[sudo] password for murashovava: 
murashovava@node01:~$ sudo chown -R $USER:$USER /var/opt/ansible
```

## 2. Регистрация ключа

```bash
murashovava@node01:~$ ssh-keygen -t rsa -b 4096 -C "ansible-pull@192.168.56.66" -f ~/.ssh/id_rsa_ansible_pull
Generating public/private rsa key pair.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/murashovava/.ssh/id_rsa_ansible_pull
Your public key has been saved in /home/murashovava/.ssh/id_rsa_ansible_pull.pub
The key fingerprint is:
SHA256:PYP6A733RxDpZVMDyRo1uxsyc2QM/XIoz28iql4aQUc ansible-pull@192.168.56.66
The key's randomart image is:
+---[RSA 4096]----+
|         E .+=oo.|
|        .  .=+* .|
|       . . .oOo. |
|      . .o o=o.o |
|       oS +++=o  |
|      ..o  o=o+  |
|      .o o   o.  |
|       .* .. ..o |
|      .+o+..o.o  |
+----[SHA256]-----+
```

