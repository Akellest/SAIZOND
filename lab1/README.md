## Quarto

Quarto enables you to weave together content and executable code into a
finished document. To learn more about Quarto see <https://quarto.org>.

## Running Code

When you click the **Render** button a document will be generated that
includes both content and the output of embedded code. You can embed
code like this:

Версия ядра

    uname -r

    ## 4.4.0-19041-Microsoft

Все сведения о ядре

    uname -a

    ## Linux ADMIN-PC 4.4.0-19041-Microsoft #2311-Microsoft Tue Nov 08 17:09:00 PST 2022 x86_64 x86_64 x86_64 GNU/Linux

release info

    lsb_release -a

    ## LSB Version: core-11.1.0ubuntu4-noarch:security-11.1.0ubuntu4-noarch
    ## Distributor ID:  Ubuntu
    ## Description: Ubuntu 22.04.2 LTS
    ## Release: 22.04
    ## Codename:    jammy

release info

    cat /etc/*release*

    ## DISTRIB_ID=Ubuntu
    ## DISTRIB_RELEASE=22.04
    ## DISTRIB_CODENAME=jammy
    ## DISTRIB_DESCRIPTION="Ubuntu 22.04.2 LTS"
    ## PRETTY_NAME="Ubuntu 22.04.2 LTS"
    ## NAME="Ubuntu"
    ## VERSION_ID="22.04"
    ## VERSION="22.04.2 LTS (Jammy Jellyfish)"
    ## VERSION_CODENAME=jammy
    ## ID=ubuntu
    ## ID_LIKE=debian
    ## HOME_URL="https://www.ubuntu.com/"
    ## SUPPORT_URL="https://help.ubuntu.com/"
    ## BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
    ## PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
    ## UBUNTU_CODENAME=jammy

Модель процессора

    cat /proc/cpuinfo | grep "model name"

    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor             
    ## model name   : AMD Ryzen 5 5600X 6-Core Processor
