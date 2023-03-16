## R Markdown

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
    ## Description: Ubuntu 22.04.1 LTS
    ## Release: 22.04
    ## Codename:    jammy

release info

    cat /etc/*release*

    ## DISTRIB_ID=Ubuntu
    ## DISTRIB_RELEASE=22.04
    ## DISTRIB_CODENAME=jammy
    ## DISTRIB_DESCRIPTION="Ubuntu 22.04.1 LTS"
    ## PRETTY_NAME="Ubuntu 22.04.1 LTS"
    ## NAME="Ubuntu"
    ## VERSION_ID="22.04"
    ## VERSION="22.04.1 LTS (Jammy Jellyfish)"
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

Последние 30 строк кольцевого буфера ядра

    dmesg | tail -n 30

    ## [    0.008370]  Microsoft 4.4.0-19041.2311-Microsoft 4.4.35
    ## [    0.069987] <3>init: (1) ERROR: ConfigInitializeCommon:665: Failed to mount /usr/lib/wsl/drive
    ## [    0.069990] : 19
    ## [    0.070055] <3>init: (1) ERROR: ConfigInitializeCommon:665: Failed to mount /usr/lib/wsl/lib
    ## [    0.070057] 19

This is an R Markdown document. Markdown is a simple formatting syntax
for authoring HTML, PDF, and MS Word documents. For more details on
using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that
includes both content as well as the output of any embedded R code
chunks within the document. You can embed an R code chunk like this:

    summary(cars)

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

## Including Plots

You can also embed plots, for example:

![](readme_files/figure-markdown_strict/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
