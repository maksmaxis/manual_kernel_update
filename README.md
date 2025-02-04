```
# manual_kernel_update centos-7.7.1908 Vagrant box
# v1.0 currently released version
# version of kernel Centos 7.7 6.0.7-1.el7.elrepo.x86_64 
# virtualbox Hosted by Vagrant Cloud (841 MB) Provided 
```

**How to use this box with Vagrant:**


Vagrantfile
```
Vagrant.configure("2") do |config|
  config.vm.box = "urenat/centos-7.7.1908"
  config.vm.box_version = "1.0"
end
```

Первым шагом для Vagrant является создание корневой директории проекта и инициализация проекта:
```
$ mkdir ~/otus
```
Переходим в нашу директорию:
```
$ cd ~/otus
```
Загрузить репозиторий из github: 
```
$ git clone https://github.com/maksmaxis/manual_kernel_update.git
```
Загружаем первую виртуальную машину Vagrant и вводим команду:
```
$ vagrant up
```
Чтобы проверить его работоспособность производится подключение SSH к виртуальной машине: 
```
$ vagrant ssh
```
После успешного входа в VM можем проверить версию ядра командой:
```
$ uname -r
```
```
Вывод:
[vagrant@localhost ~]$ uname -r 
6.0.7-1.el7.elrepo.x86_64
```
Выходим из виртуальной машины:
```
logout
```
После мы можем проверить бокc командой:
```
$ vagrant box list | grep 1908
```
```
urenat/centos-7.7.1908 (virtualbox, 1.0)
```
Остановка работы среды:
```
$ vagrant halt
```
Следующая строка остановит работу среды, а также очистит всю информацию, которая была необходима для ее работы:
```
$ vagrant destroy
```
