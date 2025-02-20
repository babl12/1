# Конфиг для пользовательских машин:
# for apt
# sudo nano /etc/apt/sources.list 
```
#deb cdrom:[Ubuntu 22.04.4 LTS _Jammy Jellyfish_ - Release amd64 (20240220)]/ jammy main restricted

# See http://help.ubuntu.com/community/UpgradeNotes for how to upgrade to
# newer versions of the distribution.
deb http://192.168.0.4:8081/repository/apt1/ jammy main restricted
deb-src http://192.168.0.4:8081/repository/apt1/ jammy main restricted

## Major bug fix updates produced after the final release of the
## distribution.
deb http://192.168.0.4:8081/repository/apt1/ jammy-updates main restricted
deb-src http://192.168.0.4:8081/repository/apt1/ jammy-updates main restricted

## N.B. software from this repository is ENTIRELY UNSUPPORTED by the Ubuntu
## team. Also, please note that software in universe WILL NOT receive any
## review or updates from the Ubuntu security team.
deb http://192.168.0.4:8081/repository/apt1/ jammy universe
deb-src http://192.168.0.4:8081/repository/apt1/ jammy universe
deb http://192.168.0.4:8081/repository/apt1/ jammy-updates universe
deb-src http://192.168.0.4:8081/repository/apt1/ jammy-updates universe

## N.B. software from this repository is ENTIRELY UNSUPPORTED by the Ubuntu 
## team, and may not be under a free licence. Please satisfy yourself as to 
## your rights to use the software. Also, please note that software in 
## multiverse WILL NOT receive any review or updates from the Ubuntu
## security team.
deb http://192.168.0.4:8081/repository/apt1/ jammy multiverse
deb-src http://192.168.0.4:8081/repository/apt1/ jammy multiverse
deb http://192.168.0.4:8081/repository/apt1/ jammy-updates multiverse
deb-src http://192.168.0.4:8081/repository/apt1/ jammy-updates multiverse

## N.B. software from this repository may not have been tested as
## extensively as that contained in the main release, although it includes
## newer versions of some applications which may provide useful features.
## Also, please note that software in backports WILL NOT receive any review
## or updates from the Ubuntu security team.
deb http://192.168.0.4:8081/repository/apt1/ jammy-backports main restricted universe multiverse
deb-src http://192.168.0.4:8081/repository/apt1/ jammy-backports main restricted universe multiverse

deb http://192.168.0.4:8081/repository/apt2/ jammy-security main restricted
deb-src http://192.168.0.4:8081/repository/apt2/ jammy-security main restricted
deb http://192.168.0.4:8081/repository/apt2/ jammy-security universe
# deb-src http://security.ubuntu.com/ubuntu jammy-security universe
deb http://192.168.0.4:8081/repository/apt2/ jammy-security multiverse
deb-src http://192.168.0.4:8081/repository/apt2/ jammy-security multiverse

# This system was installed using small removable media
# (e.g. netinst, live or single CD). The matching "deb cdrom"
# entries were disabled at the end of the installation process.
# For information about how to configure apt package sources,
# see the sources.list(5) manual.
#deb cdrom:[Ubuntu 22.04.4 LTS _Jammy Jellyfish_ - Release amd64 (20240220)]/ jammy main restricted

# See http://help.ubuntu.com/community/UpgradeNotes for how to upgrade to
# newer versions of the distribution.
deb http://ru.archive.ubuntu.com/ubuntu/ jammy main restricted
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy main restricted

## Major bug fix updates produced after the final release of the
## distribution.
deb http://ru.archive.ubuntu.com/ubuntu/ jammy-updates main restricted
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy-updates main restricted

## N.B. software from this repository is ENTIRELY UNSUPPORTED by the Ubuntu
## team. Also, please note that software in universe WILL NOT receive any
## review or updates from the Ubuntu security team.
deb http://ru.archive.ubuntu.com/ubuntu/ jammy universe
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy universe
deb http://ru.archive.ubuntu.com/ubuntu/ jammy-updates universe
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy-updates universe

## N.B. software from this repository is ENTIRELY UNSUPPORTED by the Ubuntu 
## team, and may not be under a free licence. Please satisfy yourself as to 
## your rights to use the software. Also, please note that software in 
## multiverse WILL NOT receive any review or updates from the Ubuntu
## security team.
deb http://ru.archive.ubuntu.com/ubuntu/ jammy multiverse
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy multiverse
deb http://ru.archive.ubuntu.com/ubuntu/ jammy-updates multiverse
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy-updates multiverse

## N.B. software from this repository may not have been tested as
## extensively as that contained in the main release, although it includes
## newer versions of some applications which may provide useful features.
## Also, please note that software in backports WILL NOT receive any review
## or updates from the Ubuntu security team.
deb http://ru.archive.ubuntu.com/ubuntu/ jammy-backports main restricted universe multiverse
deb-src http://ru.archive.ubuntu.com/ubuntu/ jammy-backports main restricted universe multiverse

deb http://security.ubuntu.com/ubuntu jammy-security main restricted
deb-src http://security.ubuntu.com/ubuntu jammy-security main restricted
deb http://security.ubuntu.com/ubuntu jammy-security universe
# deb-src http://security.ubuntu.com/ubuntu jammy-security universe
deb http://security.ubuntu.com/ubuntu jammy-security multiverse
deb-src http://security.ubuntu.com/ubuntu jammy-security multiverse

# This system was installed using small removable media
# (e.g. netinst, live or single CD). The matching "deb cdrom"
# entries were disabled at the end of the installation process.
# For information about how to configure apt package sources,
# see the sources.list(5) manual.
```
# for pip
# sudo nano /etc/pip.conf
```
[global]
index=http://192.168.0.4:8081/repository/pypiprox/pypi
extra-index-url=http://192.168.0.4:8081/repository/pypiprox/simple\
trusted-host=192.168.0.4
```
# for docker 
# sudo nano /etc/docker/daemon.json
```
{
  "registry-mirrors": ["https://192.168.0.4"],
  "insecure-registries": ["192.168.0.4"]
}
```
## Посмотреть загруженные пакеты можно:
![image](https://github.com/user-attachments/assets/3131b8e8-be17-4781-9648-9dcb237ed5ee)
# Далее заходим под user: admin pass:123( не обязательно для просмотра пакетов)
![da](https://github.com/user-attachments/assets/c796f57d-95d0-46ba-bb74-768c76c4095f)
# Жмём на 1 потом на browse и тут показы репозитории, кликнув на которые покажется их содержимое, например при нажатии на dockerhubprox откроется следующее:
![image](https://github.com/user-attachments/assets/e06b3eec-1023-4a77-972b-460eb4ef01dd)


