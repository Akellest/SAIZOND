Untitled
================

Версия ядра

``` bash
uname -r
```

    4.4.0-19041-Microsoft

Все сведения о ядре

``` bash
uname -a
```

    Linux ADMIN-PC 4.4.0-19041-Microsoft #2311-Microsoft Tue Nov 08 17:09:00 PST 2022 x86_64 x86_64 x86_64 GNU/Linux

release info

``` bash
lsb_release -a
```

    LSB Version:    core-11.1.0ubuntu4-noarch:security-11.1.0ubuntu4-noarch
    Distributor ID: Ubuntu
    Description:    Ubuntu 22.04.2 LTS
    Release:    22.04
    Codename:   jammy

release info

``` bash
cat /etc/*release*
```

    DISTRIB_ID=Ubuntu
    DISTRIB_RELEASE=22.04
    DISTRIB_CODENAME=jammy
    DISTRIB_DESCRIPTION="Ubuntu 22.04.2 LTS"
    PRETTY_NAME="Ubuntu 22.04.2 LTS"
    NAME="Ubuntu"
    VERSION_ID="22.04"
    VERSION="22.04.2 LTS (Jammy Jellyfish)"
    VERSION_CODENAME=jammy
    ID=ubuntu
    ID_LIKE=debian
    HOME_URL="https://www.ubuntu.com/"
    SUPPORT_URL="https://help.ubuntu.com/"
    BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
    PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
    UBUNTU_CODENAME=jammy

Модель процессора

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             
    model name  : AMD Ryzen 5 5600X 6-Core Processor             

Последние 30 строк кольцевого буфера ядра

``` bash
dmesg | tail -n 30
```

    [    0.009118]  Microsoft 4.4.0-19041.2311-Microsoft 4.4.35
    [    0.067528] <3>init: (1) ERROR: ConfigInitializeCommon:665: Failed to mount /usr/lib/wsl/drive
    [    0.067532] : 19
    [    0.067596] <3>init: (1) ERROR: ConfigInitializeCommon:665: Failed to mount /usr/lib/wsl/lib
    [    0.067598] 19

The `echo: false` option disables the printing of code (only output is
displayed).
