Poznamky na skusku LPIC3-304-200 - Virtualization & High Availability
-----------

#### Uvod:

Poznamky su rozdelene na dve hlavne casti (oddelene ciarou):
1. Zaklady operacneho systemu GNU/Linux
2. Poznamky k predmetnym temam certifikacnej skusky LPIC3 304-200

### Obsah:

* [Poznamky na skusku LPIC3-304-200 - Virtualization &amp; High Availability](#poznamky-na-skusku-lpic3-304-200---virtualization--high-availability)
  * [Obsah](#obsah)
  * [Moj skromny nazor na priority pri realizacii projektov na OS GNU/Linux](#moj-skromny-nazor-na-priority-pri-realizacii-projektov-na-os-gnulinux)
* * *

* [Zakladne tipy a triky pre operacny system GNU/Linux](#zakladne-tipy-a-triky-pre-operacny-system-gnulinux)
  * [Zakladne nastavenie siete v systeme Debian11](#zakladne-nastavenie-siete-v-systeme-debian11)
  * [Dodatok k nastaveniu statickej IPv6 adrese v systeme Debian11](#dodatok-k-nastaveniu-statickej-ipv6-adrese-v-systeme-debian11)
  * [Nastavenie siete v systeme CentOS](#nastavenie-siete-v-systeme-centos)
  * [Nastavenie siete v systeme Fedora 35 Server](#nastavenie-siete-v-systeme-fedora-35-server)
  * [Ako konfigurovat siet v systeme Ubuntu 20.04](#ako-konfigurovat-siet-v-systeme-ubuntu-2004)
  * [Zaklady spravy diskov, particii a SWAP priestoru](#zaklady-spravy-diskov-particii-a-swap-priestoru)
    * [Zaklady prace s LVM, aktualna verzia je LVM2](#zaklady-prace-s-lvm-aktualna-verzia-je-lvm2)
    * [Zaklady prace so suborovymi <em>inode-mi</em>](#zaklady-prace-so-suborovymi-inode-mi)
    * [Zaklady prace s boot-loaderom GRUB2](#zaklady-prace-s-boot-loaderom-grub2)
  * [Zaklady prace s inicializacnym systemom <em>SystemD</em>](#zaklady-prace-s-inicializacnym-systemom-systemd)
    * [Logovanie a diagnostika user-space nastrojov](#logovanie-a-diagnostika-user-space-nastrojov)
  * [Tipy k praci s uzivatelskymi uctami](#tipy-k-praci-s-uzivatelskymi-uctami)
  * [Cron a planovanie v kratkosti](#cron-a-planovanie-v-kratkosti)
  * [Praca s monitorovanim procesov/programov](#praca-s-monitorovanim-procesovprogramov)
  * [Praca so sietovymi nastrojmi (IPv4, IPv6, DNS)](#praca-so-sietovymi-nastrojmi-ipv4-ipv6-dns)
  * [Praca s TCP/UDP aplikaciami, socketmi](#praca-s-tcpudp-aplikaciami-socketmi)
* [Praca s BASH skriptami, interpretom a dalsimi nastrojmi v prostredi GNU/Linux](#praca-s-bash-skriptami-interpretom-a-dalsimi-nastrojmi-v-prostredi-gnulinux)
  * [Prikazovy interpret BASH ma specialne premenne pre argumenty, napr. skript ashow.sh](#prikazovy-interpret-bash-ma-specialne-premenne-pre-argumenty-napr-skript-ashowsh)
  * [Priklad na riadenie toku v BASH skripte s prikazom `if`](#priklad-na-riadenie-toku-v-bash-skripte-s-prikazom-if)
  * [Dalsie poznamky k zakladom prace v BASH terminale/interprete a prostredi OS GNU/Linux](#dalsie-poznamky-k-zakladom-prace-v-bash-terminaleinterprete-a-prostredi-os-gnulinux)
  * [Priklad na cvicny input error handling (osetrenie chybneho vstupu) v jazyku BASH](#priklad-na-cvicny-input-error-handling-osetrenie-chybneho-vstupu-v-jazyku-bash)
  * [Cvicny skript nacita vo `for` slucke hodnoty z `.txt` suboru do premennej `$ip`](#priklad-bash-skript-nacita-vo-for-slucke-hodnoty-z-txt-suboru-do-premennej-ip)
  * [Ako vytvorit skript s jednoduchym *select* menu v jazyku BASH](#ako-vytvorit-skript-s-jednoduchym-select-menu-v-jazyku-bash)
  * [Jednoduchy priklad na hladanie substringu zo systemoveho vypisu](#jednoduchy-priklad-na-hladanie-substringu-zo-systemoveho-vypisu)
  * [Dalsie zdroje k zakladom BASH skriptov](#dalsie-zdroje-k-zakladom-bash-skriptov)
  * [Praca s prenosom suborov po sieti](#praca-s-prenosom-suborov-po-sieti)
  * [Praca s projektom *SSHFS - SSH File System*](#praca-s-projektom-sshfs---ssh-file-system)
  * [Praca s premennymi prostredia v interprete BASH](#praca-s-premennymi-prostredia-v-interprete-bash)
* [Zaklady prace s vyvojarskymi nastrojmi](#zaklady-prace-s-vyvojarskymi-nastrojmi)
  * [Jednoduchy priklad ako kompilovat zdrojove subory v jazyku <em>C</em>](#jednoduchy-priklad-ako-kompilovat-zdrojove-subory-v-jazyku-c)
  * [Jednoduchy priklad ako kompilovat zdrojove subory v jazyku <em>Java</em>](#jednoduchy-priklad-ako-kompilovat-zdrojove-subory-v-jazyku-java)
  * [Ako kompilovat a instalovat distribuovane zdrojove baliky](#ako-kompilovat-a-instalovat-distribuovane-zdrojove-baliky)
* [Zaklady prace s virtualnymi kontajnermi, projekt Docker](#zaklady-prace-s-virtualnymi-kontajnermi-projekt-docker)
  * [Zakladne prikazy pre nastroj Docker](#zakladne-prikazy-pre-nastroj-docker)
  * [Dalsie poznamky k praci s Docker-om](#dalsie-poznamky-k-praci-s-docker-om)
* [Zaklady prace s nastrojom Git a platformou GitHub](#zaklady-prace-s-nastrojom-git-a-platformou-github)
    * [Ako replikovat lokalny Git repozitar na vzdialeny server, napr. na GitHub](#ako-replikovat-lokalny-git-repozitar-na-vzdialeny-server-napr-na-github)
* [Zaklady bezpecnosti v operacnom systeme GNU/Linux](#zaklady-bezpecnosti-v-operacnom-systeme-gnulinux)
    * [Nastroj na ochranu/kontrolu integrity suborov a adresarov, projekt <em>AIDE</em>](#nastroj-na-ochranukontrolu-integrity-suborov-a-adresarov-projekt-aide)
    * [Na overovanie bezpecnosti hesla mozeme pouzit nastroj <em>John the Ripper</em>](#na-overovanie-bezpecnosti-hesla-mozeme-pouzit-nastroj-john-the-ripper)
    * [Dalsie politiky hesla, napr. jeho zlozitost spravuju <em>PAM - Pluggable Authentification Modules</em>](#dalsie-politiky-hesla-napr-jeho-zlozitost-spravuju-pam---pluggable-authentification-modules)
    * [Ako vytvorit sifrovanu particiu na HDD/SSD](#ako-vytvorit-sifrovanu-particiu-na-hddssd)
    * [Zaklady prace s nastrojom sudo](#zaklady-prace-s-nastrojom-sudo)
    * [V oblasti <em>Steganografie</em> sa pouziva nastroj `steghide`](#v-oblasti-steganografie-sa-pouziva-nastroj-steghide)
    * [Dalsie priklady prace s uzivatelskymi uctami](#dalsie-priklady-prace-s-uzivatelskymi-uctami)
    * [Zaklady prace s programom nmap](#zaklady-prace-s-programom-nmap)
    * [Nastroje na detekciu tzv. <em>Rootkit-ov</em>](#nastroje-na-detekciu-tzv-rootkit-ov)
    * [Ako hladat/mazat virusy, pouzijeme projekt <em>Clam-AV</em>](#ako-hladatmazat-virusy-pouzijeme-projekt-clam-av)
    * [Ako na zabezpecnie zavadzaca <em>GRUB2</em>](#ako-na-zabezpecnie-zavadzaca-grub2)
    * [Zabezpecenie servera <em>OpenSSH</em>](#zabezpecenie-servera-openssh)
    * [Ako zabranit tzv. <em>Fork bomb-am</em>](#ako-zabranit-tzv-fork-bomb-am)
    * [Ako zasifrovat subor s citlivymi udajmi pomocou projektu <em>GNU-PG</em>](#ako-zasifrovat-subor-s-citlivymi-udajmi-pomocou-projektu-gnu-pg)
* [Zaklady prace s DNS serverom BIND 9](#zaklady-prace-s-dns-serverom-bind-9)
* [Zaklady prace s webovym serverom Apache2](#zaklady-prace-s-webovym-serverom-apache2)
  * [Ako zadefinovat tzv. <em>Virtual Hosting</em> pre Web server Apache2](#ako-zadefinovat-tzv-virtual-hosting-pre-web-server-apache2)
  * [Ako nainstalovat podporu PHP na server Apache2](#ako-nainstalovat-podporu-php-na-server-apache2)
  * [Ako zapnut v Apache2 modul na kompresiu posielaneho obsahu](#ako-zapnut-v-apache2-modul-na-kompresiu-posielaneho-obsahu)
  * [Ako zapnut vstavane monitorovanie servera Apache2](#ako-zapnut-vstavane-monitorovanie-servera-apache2)
  * [Ako zablokovat na Apache2 indexovy vypis suborov, tzv. *file listing*](#ako-zablokovat-na-apache2-indexovy-vypis-suborov-tzv-file-listing)
* [Zaklady prace s automatizacnym nastrojom Ansible](#zaklady-prace-s-automatizacnym-nastrojom-ansible)
* [Zaklady prace s balickovacim systemom <em>Zypper</em> v systeme OpenSUSE Leap](#zaklady-prace-s-balickovacim-systemom-zypper-v-systeme-opensuse-leap)
* [Zaklady prace so SAN protokolom iSCSI](#zaklady-prace-so-san-protokolom-iscsi)
  * [Vytvorenie iSCSI targetu <em>(SAN-server)</em> na OS Fedora Server 35](#vytvorenie-iscsi-targetu-san-server-na-os-fedora-server-35)
  * [Vytvorenie iSCSI initiatora <em>(SAN-klient)</em> na OS OpenSUSE Leap 15.3](#vytvorenie-iscsi-initiatora-san-klient-na-os-opensuse-leap-153)
* * *

* [Zaklady prace s HA - High Availability Cultermi v systeme GNU/Linux](#zaklady-prace-s-ha---high-availability-cultermi-v-systeme-gnulinux)
  * [Trocha teorie: CIB - Cluster Information Base, Stav Clustra v pamati systemu](#trocha-teorie-cib---cluster-information-base-stav-clustra-v-pamati-systemu)
  * [Priklad instalacie Multicast clustra na systeme OpenSUSE Leap s nastrojom crm:](#priklad-instalacie-multicast-clustra-na-systeme-opensuse-leap-s-nastrojom-crm)
  * [Dalsia praca s nastrojom crm:](#dalsia-praca-s-nastrojom-crm)
  * [Praca s RA - Resource Agents:](#praca-s-ra---resource-agents)
  * [Priklad instalacie Unicast clustra v systeme CentOS Stream 9 - nastroj pcs:](#priklad-instalacie-unicast-clustra-v-systeme-centos-stream-9---nastroj-pcs)
  * [Dalsia praca s Cluster nastrojom `pcs`:](#dalsia-praca-s-cluster-nastrojom-pcs)
  * [Zjednoduseny priklad ako vytvorit WebServer cluster pomocou crm na OS OpenSUSE Leap 15.3:](#zjednoduseny-priklad-ako-vytvorit-webserver-cluster-pomocou-crm-na-os-opensuse-leap-153)
  * [Zjednoduseny priklad ako vytvorit WebServer cluster pomocou pcs na CentOS Stream 9:](#zjednoduseny-priklad-ako-vytvorit-webserver-cluster-pomocou-pcs-na-centos-stream-9)
  * [Pri zostavovani clustra nastrojom pcs:](#pri-zostavovani-clustra-nastrojom-pcs)
  * [V distribucii OpenSUSE je konfiguracia Cluster kvora:](#v-distribucii-opensuse-je-konfiguracia-cluster-kvora)
  * [Zaklady konceptu Node Fencing/STONITH:](#zaklady-konceptu-node-fencingstonith)
  * [Konfiguracia Fencing-u v systeme CentOS Stream 9:](#konfiguracia-fencing-u-v-systeme-centos-stream-9)
  * [Ako pouzivat SBD Fencing na VM:](#ako-pouzivat-sbd-fencing-na-vm)
  * [Praca s <em>Cluster Resources</em>, teda zdroje, ktore dokaze cluster poskytovat:](#praca-s-cluster-resources-teda-zdroje-ktore-dokaze-cluster-poskytovat)
    * [Praca s obmedzeniami zdrojov <em>Resource constraints</em>:](#praca-s-obmedzeniami-zdrojov-resource-constraints)
    * [Praca s cluster obmedzeniami pomocou konceptu <em>Resource Groups</em>:](#praca-s-cluster-obmedzeniami-pomocou-konceptu-resource-groups)
    * [Praca s konceptom <em>Cluster Resource Clones</em>:](#praca-s-konceptom-cluster-resource-clones)
    * [Priklad ako vytvorit Cluster s <em>FTP server zdrojom</em> pomocou pcs:](#priklad-ako-vytvorit-cluster-s-ftp-server-zdrojom-pomocou-pcs)
    * [Priklad tvorby zdrojov clustera s obmedzeniami/constraints pomocou nastroja crm:](#priklad-tvorby-zdrojov-clustera-s-obmedzeniamiconstraints-pomocou-nastroja-crm)
    * [Zaklady manazmentu zdrojov Clustera s nastrojmi pcs a crm:](#zaklady-manazmentu-zdrojov-clustera-s-nastrojmi-pcs-a-crm)
    * [Dalsie tipy a triky pre nastroje crm a pcs na spravu uzlov a zdrojov v Clustroch:](#dalsie-tipy-a-triky-pre-nastroje-crm-a-pcs-na-spravu-uzlov-a-zdrojov-v-clustroch)
    * [Praca s Cluter logmi projektov <em>Corosync</em> a <em>Pacemaker</em>:](#praca-s-cluter-logmi-projektov-corosync-a-pacemaker)
    * [Dalsie priklady na manazment Clustra s nastrojom pcs:](#dalsie-priklady-na-manazment-clustra-s-nastrojom-pcs)
    * [Dalsie priklady na manazment Clustra s nastrojom crm:](#dalsie-priklady-na-manazment-clustra-s-nastrojom-crm)
* [Zaklady prace so <em>Storage</em> rieseniami v Cluster prostredi GNU/Linux](#zaklady-prace-so-storage-rieseniami-v-cluster-prostredi-gnulinux)
  * [Ako na instalaciu/nasadenie technologie <em>iSCSI Multipath</em>:](#ako-na-instalaciunasadenie-technologie-iscsi-multipath)
  * [Priklad instalacie riesenia <em>Device Mapper Multipath</em> v OS CentOS Stream 9:](#priklad-instalacie-riesenia-device-mapper-multipath-v-os-centos-stream-9)
  * [Ako zabezpecit, aby sa system Ubuntu 20.04 neplnil log spravami multipathd:](#ako-zabezpecit-aby-sa-system-ubuntu-2004-neplnil-log-spravami-multipathd)
  * [Praca s Cluster Storage riesenim <em>DRBD - Distributed Replicated Block Device</em>:](#praca-s-cluster-storage-riesenim-drbd---distributed-replicated-block-device)
  * [Instalacia technologie DRBD v systeme OpenSUSE 15.3:](#instalacia-technologie-drbd-v-systeme-opensuse-153)
  * [Zaklady prace s Cluster suborovym systemom GFS2 (Global File System):](#zaklady-prace-s-cluster-suborovym-systemom-gfs2-global-file-system)
    * [Priprava pre zaklady prace s LVM v Cluster prostredi:](#priprava-pre-zaklady-prace-s-lvm-v-cluster-prostredi)
    * [Priprava pred instalaciou GFS2 na RedHat based systemoch (CentOS/Rocky Linux):](#priprava-pred-instalaciou-gfs2-na-redhat-based-systemoch-centosrocky-linux)
* [Priklad na WebServer Cluster pomocou Pacemaker a GFS2 na OS Rocky Linux 8.5:](#priklad-na-webserver-cluster-pomocou-pacemaker-a-gfs2-na-os-rocky-linux-85)
* [NFS Server v Cluster rieseni na Rocky Linux 8.5, so zdielanym LVM cez iSCSI:](#nfs-server-v-cluster-rieseni-na-rocky-linux-85-so-zdielanym-lvm-cez-iscsi)
* [Zaklady konceptu <em>Load-Balancing</em> v Cluster prostredi OS GNU/Linux](#zaklady-konceptu-load-balancing-v-cluster-prostredi-os-gnulinux)
  * [Praca s Load-Balancingom, teda rozkladanim zataze na viacero aplikacnych uzlov:](#praca-s-load-balancingom-teda-rozkladanim-zataze-na-viacero-aplikacnych-uzlov)
  * [Zjednoduseny priklad instalacie load-balancera HAProxy na OS Rocky Linux 8.5:](#zjednoduseny-priklad-instalacie-load-balancera-haproxy-na-os-rocky-linux-85)
* [Praca s <em>virtualizacnymi nastrojmi</em> pre OS GNU/Linux](#praca-s-virtualizacnymi-nastrojmi-pre-os-gnulinux)
  * [Praca s virtualizacnou platformou Xen:](#praca-s-virtualizacnou-platformou-xen)
    * [Priklad ako vytvorit HVM (Hardware Virtual Machine) instanciu s instalacnym .iso suborom:](#priklad-ako-vytvorit-hvm-hardware-virtual-machine-instanciu-s-instalacnym-iso-suborom)
  * [Praca s virtualizacnou platformou <em>KVM</em> a pridruzenymi projektami <em>QEMU</em> a <em>libvirt</em>:](#praca-s-virtualizacnou-platformou-kvm-a-pridruzenymi-projektami-qemu-a-libvirt)
    * [Zjednoduseny priklad, ako instalovat KVM + QEMU na Host pocitaci/servery s OS Rocky Linux 8.5:](#zjednoduseny-priklad-ako-instalovat-kvm--qemu-na-host-pocitaciservery-s-os-rocky-linux-85)
  * [Zaklady prace s <em>OS-level virtualization</em> projektami <em>OpenVZ</em> a <em>LXC</em>:](#zaklady-prace-s-os-level-virtualization-projektami-openvz-a-lxc)
    * [Praca s projektom <em>OpenVZ</em>, ktory pracuje s kontajnermi:](#praca-s-projektom-openvz-ktory-pracuje-s-kontajnermi)
    * [Praca s virtualizacnou platformou <em>LXC - Linux Containers</em>:](#praca-s-virtualizacnou-platformou-lxc---linux-containers)
    * [Virtualizacny nastroj <em>VirtualBox</em>:](#virtualizacny-nastroj-virtualbox)
    * [Nastroj <em>Packer</em> sluzi na automatizovanu tvorbu a konfiguraciu VM imagov:](#nastroj-packer-sluzi-na-automatizovanu-tvorbu-a-konfiguraciu-vm-imagov)
    * [Nastroj <em>Vagrant</em> sa vyuziva:](#nastroj-vagrant-sa-vyuziva)
* [Praca s kniznicou/nastrojmi/API pod nazvom projektu libvirt:](#praca-s-kniznicounastrojmiapi-pod-nazvom-projektu-libvirt)
* [Praca s VM hosting stackom z komponentov <em>KVM,  QEMU, libvirt</em> na OS Rocky Linux 8.5:](#praca-s-vm-hosting-stackom-z-komponentov-kvm--qemu-libvirt-na-os-rocky-linux-85)
* [Praca so sadou virtualizacnych nastrojov pod nazvom projektu <em>oVirt</em>:](#praca-so-sadou-virtualizacnych-nastrojov-pod-nazvom-projektu-ovirt)
  * [Zjednoduseny postup instalacie oVirt prostredia s NFS storage riesenim na OS Rocky Linux 8.5:](#zjednoduseny-postup-instalacie-ovirt-prostredia-s-nfs-storage-riesenim-na-os-rocky-linux-85)
* [Poznamky k projektu OpenStack:](#poznamky-k-projektu-openstack)
* [Poznamky k projektu CloudStack:](#poznamky-k-projektu-cloudstack)
* [Projekt Eucalyptus:](#projekt-eucalyptus)
* [Projekt OpenNebula:](#projekt-opennebula)
* [Nezaradene poznamky pre system GNU/Linux](#nezaradene-poznamky-pre-system-gnulinux)
  * [Ako v systeme GNU/Linux vypnut HW PC-speaker:](#ako-v-systeme-gnulinux-vypnut-hw-pc-speaker)
  * [Dobra stranka na zaciatocnu konfiguraciu znamych distribucii Linuxu:](#dobra-stranka-na-zaciatocnu-konfiguraciu-znamych-distribucii-linuxu)
  * [Ak system nepreklada DNS zaznami a hlasi: "Temporary failure in name resolution"](#ak-system-nepreklada-dns-zaznami-a-hlasi-temporary-failure-in-name-resolution)
  * [Ako v Unix-like systemoch konvertovat video kodekom H.265](#ako-v-unix-like-systemoch-konvertovat-video-kodekom-h265)

* * * 
#### Moj skromny nazor na priority pri realizacii projektov na OS GNU/Linux:

    Bezpecnost + Zalohovanie + Kontrola pouzitelnosti zaloh + Dokumentacia

    + zvazit nasadenie IPv6, ak je to mozne (definitivne by uz malo byt)

* * *
Zakladne tipy a triky pre operacny system GNU/Linux
----------------------

#### Zakladne nastavenie siete v systeme Debian11:

Editujeme konf. subor: `/etc/network/interfaces`, nasledne vlozime napr.:
```
    auto lo
    iface lo inet loopback

    allow-hotplug ens33
    iface ens33 inet static
    address 192.168.1.242
    network 192.168.1.0
    netmask 255.255.255.0
    broadcast 192.168.1.255
    gateway 192.168.1.1
    dns-nameservers 193.17.47.1 185.43.135.1
```

Po uprave aplikujeme config: `$ sudo systemctl restart ifup@ens33`

#### Dodatok k nastaveniu statickej IPv6 adrese v systeme Debian11:

Bolo potrebne do suboru `/etc/sysctl.conf` vlozit riadky:

    net.ipv6.conf.ens37.autoconf = 0
    net.ipv6.conf.ens37.accept_ra = 0

Nasledne ulozit a reboot alebo prikaz: `$ sudo sysctl -p`

Potom do suboru `/etc/network/interfaces` pridat `IPv6` riadky napr.:

    auto ens37
    allow-hotplug ens37
    iface ens37 inet6 static
        address 2001:db8:cafe::242/64
        gateway 2001:db8:cafe::1
        dns-nameservers 2001:148f:ffff::1 2001:148f:fffe::1

#### Nastavenie siete v systeme CentOS:

Pouzil som nejake GNOME GUI, neviem preco sa to hned neaplikovalo.
  - alternativne sa da pouzit nastroj `nmtui`, instalujeme: `$ sudo dnf -y in NetworkManager-tui`
  - nasledne uz len spustime: `$ sudo nmtui`

#### Nastavenie siete v systeme Fedora 35 Server:

- pouzil som cli nastroj `nmcli` z balika `NetworkManager`

Nastavime hostname napr.:

    $ sudo hostnamectl set-hostname ubuntu1.example.com

Vypiseme sietove zariadenia:

    $ sudo nmcli device

Nastavime IPv4 adresu:

    $ sudo nmcli connection modify ens33 ipv4.addresses 10.0.0.30/24

Nastavime IPv4 predvolenu branu:

    $ sudo nmcli connection modify ens33 ipv4.gateway 10.0.0.1

Nastavime IPv4 adresu DNS serverov:

    $ sudo nmcli connection modify ens33 ipv4.dns "193.17.47.1 185.43.135.1"

Nastavime prehladavanie domeny, aby sme nemuseli zadavat cele FQDN:

    $ sudo nmcli connection modify ens33 ipv4.dns-search example.com

Nastavime manualnu staticku konfiguraciu rozhrania "ens33"

    $ sudo nmcli connection modify ens33 ipv4.method manual

Dalej "restartujeme" konfiguraciu rozhrania "ens33"

    $ sudo nmcli connection down ens33; nmcli connection up ens33 

Nasledne overime config:

    $ sudo nmcli device show ens33

#### Ako konfigurovat siet v systeme Ubuntu 20.04:
Treba *presunut/zalohovat* povodny konf. subor:

    $ sudo mv /etc/netplan/00-installer-config.yaml /etc/netplan/00-installer-config.yaml.disabled

Dalej vytvorime novy konf. subor:

    $ sudo vim /etc/netplan/00-installer-config.yaml

Nasledne pridame riadky napr.:

    network:
    ethernets:
        ens33:
        dhcp4: no
        addresses: [192.168.1.244/24]
        gateway4: 192.168.1.1
        nameservers:
            addresses: [193.17.47.1, 185.43.135.1]
        dhcp6: yes
    version: 2

Ulozit subor a potom zadat (prikaz vykona aj syntax check):

    $ sudo netplan try

Alebo:

    $ sudo netplan apply

### Zaklady spravy diskov, particii a SWAP priestoru:

Prikaz vypise blokove zariadenia: `$ sudo lsblk`

Prikaz vypise UUID aktivnych particii: `$ sudo blkid`

Prikaz vytvori Ext4 particiu: `$ sudo mkfs.ext4 /dev/sdb1`

Ako vytvorit Swap subor, nie particiu: 

- prikaz vypise stav Swap-u: `$ sudo free -m`
- dalej vytvorime File-IO image a pouzijeme ho ako SWAP pristor:
```bash
    $ sudo dd if=/dev/zero of=swap_file bs=1024k count=pocet_MB
    $ sudo mkswap swap_file
    $ sudo swapon swap_file
    $ sudo swapoff swap_file	<< pozor treba mat nahradnu Swap kapacitu
```

V kontexte Swap-u existuje v kerneli tzv. *OOM Killer*, ktory pri nedostatku pamate zabija procesy.
 - *OOM* - Out Of Memory

#### Zaklady prace s LVM, aktualna verzia je LVM2:
Prikaz na interaktivne CLI: `$ sudo lvm`

Nasledne mozeme pouzit: `lvm> help`

- prikaz vypise Physical Volumes: `pvs`
- prikaz detailne vypise Physical Volumes: `pvdisplay`
- prikaz vypise Volume Groups: `vgs`
- prikaz detailne vypise Volume Groups: `vgdispaly`
- prikaz vipise Logical Volumes: `lvs`
- prikaz detailne vypise Logical Volumes: `lvdisplay`

Na pracu s LVM vytvorime jednu alebo viac PV particii na realnych diskoch s nastrojmi `cfdisk`, `fdisk`, `parted`
- nasledne particiu naformatujeme pozadovanym FS napr. s: `$ sudo mkfs.XYZ` 

Prikaz vytvori VG s nazvom `vg-nas` a pouzije prve PV (particiu): `# vgcreate vg-nas /dev/sdb1`
 - nasledne rozsirime tuto VG (pool) o dalsiu PV particiu: `$ sudo vgextend vg-nas /dev/sdc1`

Prikaz vytvori LV particiu `lvnas1` z danej VG `vg-nas`: 
 
    $ sudo lvcreate --size 15g --type linear -n lvnas1 vg-nas

Prikaz naformatuje LV particiu na Ext4-FS: `$ sudo mkfs.ext4 /dev/mapper/vg--nas-lvnas1`

Prikaz rucne namountuje LV `lvnas1` do adresara `/mnt/lvnas1`:

    $ sudo mount /dev/mapper/vg--nas-lvnas1 lvnas1

Nasledne upravou suboru `/etc/fstab` pridame riadok, ktory zabezpeci mount po reboot-e:
 
Pomoze prikaz `$ sudo blkid`

    /dev/disk/by-uuid/20067ff2-0599-4fd3-9cfc-dbbd6aa07aec /mnt/lvnas1 ext4 defaults 0 1
    /dev/disk/by-uuid/4c1d7f90-0dcb-4ed1-acce-0062c2c8c186 /mnt/lvnas2 ext4 defaults 0 1

Potom si napr. v `$HOME` adresary vytvorime link na svoju NAS particiu: `$ ln -s /mnt/lvnas1 nas`

Ako ostranit LV z VG: `$ sudo lvremove vg-nas/lvnas3`

Ako zvacsit nejake LV z VG poolu (moze byt mounted): `$ sudo lvresize -r -L +5g vg-nas/lvnas1`

Overime s: `$ df -h /mnt/lvnas1`

Tip: ako pridat uzivatela do dalsej skupiny: `# usermod -a -G examplegroup exampleusername`

Tip: ako zmenit vlastnikov na adresary alebo subore: `# chown -R root:vgnas /mnt/lvnas1`

Tip: ako nastavit prava na subore alebo adresary: `# chmod g+w /mnt/lvnas1`

Tip: ako vypisat parametre kernelu, s ktorymi nabootoval: `$ cat /proc/cmdline`

Tip: ako zistit ake *kill* signaly system podporuje: `$ kill -l`

Tip: nastroj na kontrolu syntaxe BASH skriptov: `shellcheck`

#### Zaklady prace so suborovymi *inode-mi*:

Prikaz vypise prava a inode informacie o subore: `$ stat subor.xyz`

Da sa pouzit aj prikaz: `$ ls -li`

#### Zaklady prace s boot-loaderom GRUB2:

Zjednodusene konfiguracne moznosti su v subore: `/etc/default/grub`

- da sa precitat manual pre vsetky moznosti: `$ info -f grub -n 'Simple configuration'`

Zakladny konfig. subor pre GRUB2, ktory je vygenerovany a nema sa upravovat: `/boot/grub/grub.cfg`

Skripty, ktore podla poradia generuju konfig. subor GRUB2: `$ ls /etc/grub.d/*`

Ako nainstalovat GRUB2 v MBR mode: `$ sudo grub-install --boot-directory=/mnt/boot /dev/sdc`

#### Zaklady prace s inicializacnym systemom *SystemD*:

Ako vypisat logy pre proces podla urciteho string patternu: `$ journalctl --unit=ssh`

Ako vypisat status nejakeho spusteneho daemona: `$ systemctl status sshd.service`

Ako zabezpecit, aby si beziaci proces nacital novy config: `$ sudo systemctl reload sshd.service`

Ako restartovat nejaky proces: `# systemctl restart sshd.service`

Ako vypisat vsetky systemd unit-y, ktore su nacitane v RAM: `$ sudo systemctl list-units`

 - ako vypisat vsetky unit-y, ktore su nacitane aj neaktivne: `$ sudo systemctl list-units --all`

Ako vypisat vsetky unit subory pre systemd: `$ sudo systemctl list-unit-files --all`

Ako vyipsat, na com zavisi dany proces a co vyzaduje:

    $ sudo systemctl show -p Requires sshd.service
    $ sudo systemctl show -p Wants sshd.service

Nastroj na spustanie viacerych programov/skriptov v jednom adresary: `run-parts(8)`
 
- v suvislosti so starsim Init-om podla `System V Init`

Tip: Ako zistit v akom run-level-y bezi system: `$ who -r`

Tip: V akom adresary sa nachadzaju `System V Init` skripty: `$ cd /etc/rc5.d/`

Tip: Ako prepnut `run-level` do `single-user` modu: `$ sudo telinit -s`

Tip: Ako restartovat system: `$ sudo shutdown -r now`
 - pripadne za 10 min.: `$ sudo shutdown -r +10`

Tip: Ako zabezpecit, aby sa do systemu mohol prihlasit len superuser:
- vytvorime subor: `$ sudo touch /etc/nologin`

### Logovanie a diagnostika user-space nastrojov:

Ako vypisat od zaciatku log z bootovania: `$ journalctl -b`

 - pripadne v od konca do zaciatku: `$ journalctl -b -r`

 - pripadne vypisanie logu z predoslych bootov: `$ journalctl -b -1`

 - overenie, ze dany shutdown/reboot bol cisty: `$ journalctl -r -b -1`

Ako vypisat vsetky ID jednotlivych boot-ov: `$ journalctl --list-boots`

Alternativy pre logovanie v Linuxe: `syslog-ng (/etc/syslog-ng)` a `rsyslogd /etc/rsyslog.cfg)`
 
Ako vypisat, kto bol kedy naposledy prihlaseny: `$ lastlog` alebo `$ last`

Ako vypisat log pre konkretne Process ID: `$ journalctl _PID=XYZ`

Ako vypisat log spred 4 hodin: `$ journalctl -S -4h`

 - dalsi priklad presne zadaneho casu: `$ journalctl -S 06:00:00`

 - dalsi priklad presne zadaneho datumu: `$ journalctl -S 2022-01-10`

Ako vypisat logy pre konkretny proces/program/daemon/unit: `$ journalctl -u ssh`

 - pripadne prikaz vypise vsetky logovacie unit-y: `$ journalctl -F _SYSTEMD_UNIT`

Vypisovanie logov podla string match patternu: `$ journalctl -g 'kernel.'`

 - da sa skombinovat, ak chceme hladat ine logy v case okolo hladaneho stringu s: `$ journalctl -S`

Ako vypisat logy podla Severity level: `$ journalctl -p 3`

 - pripadne s rozsahom: `$ journalctl -p 2..3`

Ako sledovat real-time priebeh systemoveho logu: `$ journalctl -f`

 - logy sa daju vypisovat a sledovat napr. aj v json formate: `$ journalctl -f -o json-pretty`

Ako ulozit urcite logy v text formate: `$ journalctl -u ssh -o old > sshd.log`

 - ako ulozit rovnaky log napr. vo formate "json": `$ journalctl -u ssh -o json > sshd.log.json`

#### Tipy k praci s uzivatelskymi uctami:

Ako zmenit default shell uzivatela: `$ chsh vlkv -s /bin/bash`

 - dany SHELL by mal byt v subore: `/etc/shells`

Ako zistit s akymi argumentami je spusteny program/daemon: `$ ps aux | grep getty`

#### Cron a planovanie v kratkosti:

Ako vytvorit cron job, aby sa vystup aj error presmerovali do `/dev/null`, vytvorime zaznam: 

 - pre daneho uzivatela pouzijeme napr. prikaz: `$ crontab -e`

 - riadok zaznamu:

    `10 5 * * * /usr/bin/xyz > /dev/null 2>&1`

Ako spustit jednorazovo nejaky prikaz: `$ at 15:00`

- nasledne do promptu zadame prikaz, ukoncime s `Ctrl-d`

- naplanovane ulohy si mozeme vypisat s: `$ atq`

- tretiu ulohu mozeme vymazat s: `$ atrm 3`

Ako zadat ulohu pre systemd:

- zadame: `$ systemd-run --on-calendar='2022-01-12 16:00' /bin/echo testovacie-echo`

  - tieto docasne (transient) unit-y mozeme vypisat s: `$ systemctl list-units | grep timer`

Ako vypisat cron ulohy pre daneho uzivatela: `$ crontab -l`

#### Praca s monitorovanim procesov/programov:

Ako ovladat program `top`:

- `medzernik` obnovuje stav okamzite

- `M` usporiada procesy podla rezidentnej pamate (case sensitive)

- `T` usporiada podla celkoveho kumulativneho procesoroveho casu

- `P` default nastavenie podla aktualnej CPU zataze

- `u` zobrazi len procesy daneho uzivatela

- `?` zobrazi pomoc s interaktivnymi prikazmi

Dalsie monitorovacie alternativy su: `atop`, `htop` alebo `btop`

Ako mozeme vypisat otvorene subory, napr. pre 1 uzivatela: `$ lsof | grep student`

- vhodne pozriet: `$ man lsof`

- napr. prikaz, ktory vypise otvorene subory, pre dany PID: `$ lsof -p 1234`

- prikaz vypise otvorene sietove sockety: `$ sudo lsof -i`

- pripadne bez reverzneho prekladu DNS (da sa filtrovat s grep-om): `$ sudo lsof -n -i`

- vypisat pouzitie vsetkych suborov v danom adresary: `$ sudo lsof +D /usr/`

Ako mozeme vypisat systemove volania nejakeho programu, napr.: `$ strace cat /dev/null`

 - na presmerovanie do suboru treba pouzit err redirect: `2>`

Ako mozem vypisat nacitane kniznice nejakeho programu: `$ man 1 ltrace`

 - da sa pouzit aj program `ldd`: `$ man 8 ldd`

Ako vypisat vsetky vlakna spustenych procesov: `$ ps m`

 - vypis sa da vylepsit s: `$ ps m -o pid,tid,command`

Ako zmerat cas trvania nejakeho spusteneho programu/ulohy: `$ time <uloha>`

 - priklad: `$ time lsof +D /usr/`

Ako vypisat strom spustenych procesov: `$ ps axjf`

Ako vypisat CPU prioritu (tzv. Niceness, stlpec `NI`) spustenych procesov: `$ ps al`

 - vhodne pozriet: `$ man ps`

Ako zmenit CPU prioritu (Niceness, zhovievavost k inym procesom) daneho procesu:

 - prikaz: `$ sudo renice 20 <PID>`

 - default hodnota je `0`, rozsah je `-20` az `20`, ani hodnota `20` sa `NEDOPORUCUJE`.

 - top prioritu, teda najnizsiu zhovievavost (NEDOPORUCUJE sa) nastavime s:

   - prikaz: `$ sudo renice -20 <PID>` 

Ako vypisat stav operacnej pamate: `$ free -m`

 - je dobre si uvedomit, co je realna spotreba a co je `file cache/buffer`

Ako vypisat, ake parametre ma nastaveny kernel a system: `$ getconf -a`

#### Praca so sietovymi nastrojmi (IPv4, IPv6, DNS):

Ako vypisat sietove rozhrania a ich parametre: `$ ip address show`
 - prikaz sa da skracovat napr.: `$ ip a s`

Ako vypisat smerovaciu tabulku systemu: `$ ip route show`
 - podobne sa da skracovat: `$ ip r s`
 - smerovacuiu tab. pre IPv6 vypiseme s: `$ ip -6 route show`

Ako vypisat, akym rozhranim bude smerovany paket s danou cielovou adresou: `$ ip route get 9.9.9.9`
 - resp. pre IPv6: `$ ip -6 route get 2620:fe::9`

Ako nastavit predvolenu branu: `$ sudo ip route add default via 192.168.100.1`
 - predvolenu branu vymazeme s: `$ sudo ip route del default`
 - staticku cestu nastavime s: `$ sudo ip route add 192.168.16.0/24 via 10.1.2.3`
 - staticku cestu vymazeme s: `$ sudo ip route del 192.168.16.0/24`

Ako overit konektivitu sietoveho zariadenia: `$ ping 9.9.9.9`
 - ekvivalent pre IPv6: `$ ping6 2620:fe::9`

Ako vypisat vsetky TCP a UDP sockety: `$ sudo ss -tupa`
 - vhodne pozriet: `$ man 8 ss`

Ako vypisat reverzny PTR zaznam pre danu IP adresu: `$ host 9.9.9.9`
 - pre IPv6: `$ host 2620:fe::9`
 - pripadne detailna diagnostika: `$ dig -x 9.9.9.9`

Pozriet nastroje `NetworkManager` a `systemd.networkd(5)`

Konf. subory, ktore zabezpecuju DNS preklad: `/etc/nsswitch.conf`, `/etc/hosts`, `/etc/resolv.conf`
 - zvycajne vsak konfigurovane s inymi nastrojmi ako `Networkmanager`, `Netplan`, alebo 'nmtui'

Ako overit, ze na DNS preklady sa pouziva Cache: `$ nslookup -debug quad9.net`
 - vo vypise vidime riadky: `Server: 127.0.0.53` a `Address: 127.0.0.53#53`
 - alebo pouzijeme novsi nastroj `dig` napr.: `$ dig +trace quad9.net`
   - alebo napr.: `$ dig +trace quad9.net | grep bytes`

Ako overit nastavenia DNS v systeme: `$ resolvectl status`

Ako vypisat vsetky sietove sockety v systeme: `$ sudo netstat -tunap`

Cisla TCP/UDP portov sa daju zistit z referencneho .txt suboru `/etc/services`

Ako rucne spustit DHCP klienta: `$ sudo dhclient ens33`

Ako overit, ci je v kerneli zapnuty packet routing: `$ sysctl net.ipv4.ip_forward`
 - smerovanie IPv4 paketov zapneme s: `$ sudo sysctl -w net.ipv4.ip_forward=1`
 - smerovanie IPv6 paketov zapneme s: `$ sudo sysctl -w net.ipv6.conf.all.forwarding=1`
 - perzistentne nastavenie co prezije reboot je v subore: `/etc/sysctl.conf`
   - do suboru vlozime riadky `net.ipv4.ip_forward=1` alebo/aj `net.ipv6.conf.all.forwarding=1`
   - zmeny v subore ulozime a aplikujeme s: `$ sudo sysctl -p`

Ako vypisat pravidla firewallu IPtables: `$ sudo iptables -L`

Ako si vytvorime pravidla firewallu, vytvorime subor `/etc/network/iptables.up.rules`
Do suboru mozeme pisat riadky napr.:

    *filter
    :INPUT ACCEPT [8:631]
    :FORWARD DROP [0:0]
    :OUTPUT ACCEPT [5:576]
    -A INPUT -s 192.168.1.242/32 -j DROP
    COMMIT

Aplikujeme zmeny tak, ze ak sa "odrezeme", konf. sa obnovi po 20 sek: `$ sudo iptables-apply -t 20`

Je dobre si uvedomit, ze IPtables su nahradene komplexnym nastrojom `NFtables` (aj ked zlozitejsim) 
 - dalsie informacie: `www.netfilter.org/projects/nftables/index.html`

Ako vypisat IPv4 ARP tabulku a zaroven aj IPv6 ND tabulku: `$ ip neigh`
 - opat sa da skratit na: `$ ip n`
 - stary prikaz pre IPv4: `$ arp -an`

#### Praca s TCP/UDP aplikaciami a socketmi:

Ako vytvorit testovaci TCP socket co pocuva na danom porte: `$ sudo nc -l 23`
 - na socket sa so vzdialenej stanice pripojime napr.: `$ telnet A.B.C.D 23`
 - pripadne opat s programom `nc` napr.: `$ nc A.B.C.D 23`

Ako "stopovat" pripojenie programu `curl` k TCP HTTP socketu:
 - prikaz: `$ curl --trace-ascii tracelog.txt http://example.com`
 - nasledne si pozrieme zaznam v subore `tracelog.txt`

Ako si vygenerovat PKI par klucov na asymetricke sifrovanie a auth.: 
 - prikaz: `$ ssh-keygen -t rsa -N '' -f /home/user1/.ssh/id_rsa`
 - podobne pre DSA par klucov: `$ ssh-keygen -t dsa -N '' -f /home/user1/.ssh/id_dsa`

Pozn.: pozriet si projekty/programy `fail2ban`, pripadne `sshguard` alebo `denyhosts`

Ako pomocou protokolu SCP kopirovat z jednej vzdialenej IP na inu vzdialenu IP:
 - prikaz: `$ scp user1@host1:file user2@host2:file`

Ako vypisat vsetky TCP sockety, bez DNS prekladu adries: `$ sudo lsof -i -n`

Ako vypisat aktivne procesy pre konkretny TCP/UDP port: `$ sudo lsof -i:22`
 - daju sa pouzit aj nazvy protokolov podla suboru `/etc/services`, teda: `$ sudo lsof -i:ssh`
 - ked chceme spcifikovat len TCP sockety: `$ sudo lsof -iTCP:22`
 - ked chceme este presnejsie specifikovat pre IPv6: `$ sudo lsof -i6TCP:22`
 - este napr. bez prekladu na PTR DNS: `$ sudo lsof -n -i6:22`
 - vypise aktivne a pocuvajuce UDP "streamy": `$ sudo lsof -n -iUDP`
 - vypise stav pripojeni `protokol:port` na servery s IP `192.168.1.240` na TCP porte `22`
   - prikaz: `$ sudo lsof -iTCP@192.168.1.240:22`

Pozriet si nastroj `tcpdump`, velmi vela moznosti.
 - da sa napr. zacat s manualom: `$ man tcpdump`
 - napr. packet sniffing len ICMP paketov z/na konkretnu IPv4 adresu: 
   - prikaz: `$ sudo tcpdump -nv icmp and host 192.168.1.240`
 - napr. komunikaciu na IPv6 TCP socket na porte 22, pre interface `ens38`:
   - prikaz: `$ sudo tcpdump -nv -i ens38 ip6 and port 22`

Pozriet si nastroj `nmap`, velmi vela moznosti:
 - *POZOR* na legislativne dosledky skenovania sieti a portov, ktore nevlastnim/nespravujem
 - napr. sa da zacat s manualom: `$ man nmap`

Ako vypisat lokalne Unix Domain sockety, pre aktualneho uzivatela: `$ lsof -U`
 - vypisanie vsetkych Unix Domain socketov: `$ sudo lsof -U`

### Praca s BASH skriptami, interpretom a dalsimi nastrojmi v prostredi GNU/Linux:
Ako zabezpecit, aby sa skript spustal aj na inych systemoch (portability): 
 - skript zacina riadkom: `#!/usr/bin/env bash`
 - nevyhoda je, ze skript je spustany s prvym najdenym interpretom (BASH, Python, etc.)

V BASHi sa rozlisuje `"Quoting"` alebo `'Literals'`:
 - teda je rozdiel v prikaze: `$ echo "$100"` a v prikaze: `$ echo '$100'`
 - treba si vsak davat pozor na pouzitie s inymi programami, napr.: `$ grep 'r.*t' /etc/passwd`
   - napr. uvedeny prikaz dava neocakavany vysledok: `$ grep 'r.*t /etc/passwd'`
 - avsak pre porovnanie tieto dva prikazy:
   - prikaz 1: `$ echo "I don't like unexpected bahavior in /etc/ directory."`
   - prikaz 2: `$ echo 'I don't like unexpected bahavior in /etc/ directory.'`

Dalsi priklad rozvijania specialnych znakov v BASHi: 
 - prikaz: `$ echo "Nemam ziadnu * v mojich cestach: $PATH"`
 - porovnat s prikazom: `$ echo 'Nemam ziadnu * v mojich cestach: $PATH'`

#### Prikazovy interpret BASH ma specialne premenne pre argumenty, napr. skript `ashow.sh`:

    #!/usr/bin/env bash
    #
    # jednoduchy BASH skript demonstruje specialne premenne
    #
    echo Vypisujem prvy argument: $1
    echo Vypisujem druhy argument: $2
    echo Vypisujem treti argument: $3
    echo Vypisujem nazov skriptu: $0
    echo Vypisujem process ID skriptu: $$
    echo Vypisujem pocet odovzdanych argumentov: $#
    echo Vypisujem vsetky argumenty: $@
    #
    # koniec skriptu
    #

 - ulozime do suboru `ashow.sh` a nastavime prava, napr.: `$ chmod u+rx ashow.sh`
 - nasledne mozeme skript spustit: `$ ./ashow.sh raz dva tri`

Presmerovanie diagnostickych vypisov/vystupov:
 - Chybovy vypis/vystup mozeme presmerovat do standardneho vypisu/vystupu s: `2>&1`
 - Opacny postup: `1>&2`

Pozriet riadenie toku BASH skriptu, resp. rozhodovanie s:
 - riadiace struktury: `if`, `then`, `else`, `elif`, `while`, `until`, `case`
 - zakladny rozcestnik `$ man bash`
 - dalsi uzitocny manual: `$ man test`
 - alebo napr. `$ help if`

#### Priklad na riadenie toku v BASH skripte s prikazom `if`:
- vytvorime skript napr.: `ifPriklad.sh`:
```bash
    #!/usr/bin/env bash
    #
    # jednoduchy BASH skript demonstruje riadenie toku s "if"
    #
    # testujeme obsah prveho argumentu:
    if [ "$1" = ahoj ]
    then
        echo 'Zadany argument bol ahoj.'
    #
    # testujeme pocet zadanych argumentov:
    elif [ "$#" = 0  ]
    then
        echo "Nezadal si ziaden argument."
    #
    # pokrocilejsie testovanie regularneho vyrazu (regexp):
    elif [[ "$1" =~ a.*j  ]]
    then
        echo "Skoro dobre, zadal si argument: $1"
    #
    # posledna moznost, ked nic ine nevyhovie podmienkam:
    else
        echo "Sme vedla od slova ahoj, zadal si argument $1"
    fi
    #
    echo "Koniec skriptu, exit code: $?"
    #
```

#### Dalsie poznamky k zakladom prace v BASH terminale/interprete a prostredi OS GNU/Linux:
Ako vykonat upgrade balikov (Deb/Ubu): `$ sudo apt update -y && sudo apt upgrade -y`

Ako vymazat nepotrebne baliky (Deb/Ubu), po overeni funkcnosti:
 - prikaz: `$ sudo apt autoclean && sudo apt autoremove`

Prikazy ako `cd`, alebo `umask` su tzv. *Shell BuiltIn*, nemaju manpage, preto: `$ help cd`
 - dalsi priklad: `$ help help`
 - priklad: `$ help if`
 - priklad: `$ help jobs`

Ako prehladat manualove stranky: `$ man -k "copy files"`
 - podobne mozeme pouzit: `$ apropos "copy files"`

Ako nastavit velkost historie BASH interpretu (v RAM): `$ export HISTSIZE=2000`
 - pre subor `.bash_history` nastavime napr.: `$ export HISTFILESIZE=2000`
 
Ako nastavit do BASH historie, datum a cas: `$ export HISTTIMEFORMAT="%d/%m/%y %T "`
 - overime s prikazom: `$ history`

Ako spustit prikaz, aby sa neulozil do historie, prefixujeme ho *medzerou*: `$  prikaz`
 - napr. prikaz `$ ping linux.com` sa ulozi do historie, ale prikaz `$  ping linux.com` nie 
 - da sa nastavit premenna, aby hist. ignorovala duplicity a " ": `$ export HISTCONTROL=ignoreboth`

Ako vypisat stromovu strukturu suborov, napr.: `$ tree /home/student1 > strom.fs.student1.txt`
 - je potrebne nainstalovat balicek `tree`, dalsie informacie v: `$ man tree`

Ako vypisat (priblizne) podla velkosti adresare a subory: `$ du -hd 1 | sort`

Ako vyfiltrovat MAC adresy z vypisu a ulozit ich zaroven do suboru: 
 - prikaz: `$ ip a s | grep ether | cut -d" " -f6 | tee mac-adresy.txt`

Ako porovnat dva subory s detailnejsim rozpisom: `$ diff -c a b`
 - dva subory mmozeme porovnat vedla seba: `$ diff -y a b`
 - dalsie info v: `$ man diff`

Ako vytvorit komprimovany *BZip2* archiv: `$ tar -cvjf subory.tar.bz2 a.txt b.txt c.txt`
 - ekvivalent pre *GNUzip* kompresiu: `$ tar -cvzf subory.tar.gz a.txt b.txt c.txt`
 - mozeme kombinovat subory/adresare: `$ tar -cvzf dalsie_subory.tgz dir1/ dir2/ a.txt b.txt`
 - extrakcia do vopred vytvoreneho adresara: `$ tar -xvjf subory.tar.bz2 -C zaloha.d/`

Ako vytvorit adresarovu strukturu/hierarchiu jednym prikazom: `$ mkdir -p prvy/druhy/treti`

Ako vypisat konf. subory, zmenene za posledny den:
 - prikaz: `$ sudo find /etc -type f -mtime 0 -exec ls -l {} \;`
 - zaloha suborov, zmenenych za poslednych 7 dni:
   - prikaz  `$ sudo find /etc -type f -mtime -7 -exec cp {} /root/backup \;`
 - aby sa `find` pytal, ci chceme napr. zmazat stare subory:
   - prikaz: `$ find . -type f -mtime +30 -ok rm {} \;`
   - pripadne mozeme najskor (30 dni stare) subory len *vypisat*: `$ find . -type f -mtime +30 -print`

Ako hladat subory podla nazvu, nova implementacia `mlocate`: `$ sudo apt install mlocate`
 - databazu suborov aktualizujeme pomocou *cron-u* alebo rucne: `$ sudo updatedb`
 - stav databazy overime s: `$ mlocate -S`
 - da sa spustat aj symlinkom, napr.: `$ locate .bashrc`
 - dalsie informacie: `$ man mlocate`

Ako hladat programom `find` bez rozlisenia A/a: `$ find . -iname PriKlad.txt`

V BASH-y sa tzv. *glob-y* volaju aj *Shell Meta Characters*, napr. `*`

Prikaz najde a spocita adresare v `/etc`, hlbka 3 adresarov s pravami `755`: 
 - prikaz: `$ sudo find /etc/ -maxdepth 3 -type d -perm 755 | wc -l`

Ako vypisat subory s velkostou medzi 3G a 4G: `$ find /home/nas/ -type f -size +3G -size -4G`
 - da sa doplnit detailny vypis do suboru: 
   - prikaz: `$ find /home/nas/ -type f -size +3G -size -4G -ls > zoznam.txt`

Asociacia medzi suborovou strukturou a nazvom suboru sa nazyva tzv. *hardlink*
 - pocet asosiacii overime s: `$ stat subor.txt`
 - ako hladat hardlink-y podla cisla *inode* (index node): `$ find . -inum 12345`
 - pozor, hardlink *nemoze* opustit hranice *suboroveho systemu*
 - koncept hardlink je napr. uzitocny pre *nadradeny* adresar, oznaceny `..`

Ako naist a vypisat objekty s viac ako 1 hardlinkom: `$ find /var/ -links +1 -ls`

Ako presuvat len aktualnejsie alebo chybajuce subory: `$ mv -u <zdroj> <ciel>`

*Quiz:*
V adresary `/home/student/` vytvori uzivatel `root` subor `a.txt`, moze ho uzivatel `student` vymazat?

Prikaz najde *chybove* hlasky v Syslogu: `$ grep -win error /var/log/syslog`
 - param. `-w` hlada presne slovo, param. `-i` nerozlisuje A/a, param. `-n` vypise cislo riadku 

Ako naist v kernel ring buffery `error` a vypisat 3 riadky pred a za nim: `$ sudo dmesg | grep -C 3 error`

Zaujimavost, ako vypisat citatelne znaky v aktualnom image RAM: `$ sudo strings /dev/mem`
 - dalsie informacie v `$ man mem` a v `$ man strings`

Ako vo Vim-e spravit undo: `:e!` , alebo v "command-mode" stlacime "u"
 - vo Vim-e vlozime novy riadok s: `o`
 - ak chceme rychlo ulozit subor a ukoncit Vim, stlacime: `Shift+zz`
 - cisla riadkov zapneme s: `:set nu`
 - text oznacime v command mode s `V` + sipky, nasledne `y`, potom vlozime pod kurzor s `p`
   - alebo mozeme vystrihnut s `dd`
 - na konkretne cislo riadka sa prepneme s: `:<cislo>`
 - dva sposoby ako otvorit 2 subory: `vim -o a.txt b.txt` alebo `vim -d a.txt b.txt`
   - medzi oknami sa prepiname s `Ctrl+ww`

Ako v realnom case sledovat prihlasovanie uzivatelov: `$ sudo tail -f /var/log/auth.log`

Ako vytvorit uzivatela, ktoreho ucet exspiruje v urcity datum: `$ sudo useradd -e 2022-2-13 user1`
 - prikazom `chage` mozeme zadefinovat, kedy exspiruje heslo uzivatela

Ako pridat uzivatela `u1` do skupiny `sudo`, napr.: `$ sudo usermod -G sudo u1`
 - uziv. skupina sa neda vymazat, pokial sluzi ako primarna skupina uzivatela

*POZOR*, ako vymazat uzivatela `u1` aj s jeho *home* adresarom: `$ sudo userdel -r u1`

Ako premenovat uzivatelsku skupinu: `$ sudo groupmod -n <novy_nazov> <povodna_skupina>`

Jednoduchym prikazom `w` vypiseme zakladny stav systemu a prihlasenych uzivatelov: `$ w`
 - historicky zaznam prihlasovania uzivatelov vypiseme napr. s: `$ sudo last`
   - mozeme specifikovat aj konkretneho uzivatela `u1`, napr.: `$ sudo last u1`

Nastroj `nstat` doplna sietovu diagnostiku kernelu, je z balika `iproute2`
 - dalsie informacie `$ man nstat`, je dobre spustat takto: `$ nastat -s`

Ako overit, ci kernel kvoli teplote nepodtaktoval jadra CPU: `$ sudo dmesg | grep "cpu clock"`

*Quiz:*
Ak nastavime na subor prava `$ chmod 000 subor.txt`, moze ho niekto citat/upravovat?

Hesla ulozene (Ubu 20.04) v subore `/etc/shadow` su vo formate: `$id$salt$hash`
 - napr. identifikator (id) `6` znamena `SHA-512`

Ako vypisat atriburty (nie prava) konkretneho suboru: `$ lsattr subor.txt`
 - vyznam atributov najdeme napr. v: `$ man chattr`
 - napr. mozeme na subor nastavit tzv. `no append` atribut: `$ chattr +a subor.txt`
 - napr. mozeme nastavit tzv. `immutable` atribut, ktory *zmrazi* upravy: `$ chattr +i subor.txt`
 - atributy mozeme nastavit aj rekurzivne, pre obsah adresara: `$ sudo chattr -R dir1/`

Ako nastavit *SET UID bit*, absolutny mod `$ chmod 4XXX a.bin`, relativny mod `$ chmod u+s a.bin` 
 - overime napr. prikazom: `$ stat a.bin`
 - program/skript je spustany s pravami vlastnika, nie s pravami zadavatela prikazu
   - typicky priklad napr.: `$ cat /etc/shadow`

Ako naist subory, ktore maju *aspon* prava `4000`, zadame: `$ find /usr/bin/ -perm -4000 -ls`

Ako nastavit *SET GID bit*, absolutny mod `$ chmod 2XXX dir1/`, relativny mod `"chmod g+s dir1/`
 - subory vytvorene v adresary s *SGID bitom* budu mat vlastnika podla skupiny adresara `dir1/`
 - uzitocne pre vytvaranie zdielanych adresarov

Ako priklad mozeme vytvorit dedikovany adresar pre dvoch vyvojarov:

    # adduser dev1                       <-- vytvorime uzivatelov
    # adduser dev2
    # usermod -aG developers dev1        <-- vytvorime skupinu a zaradime uzivatelov
    # usermod -aG developers dev2
    # mkdir /repo.d                      <-- vytvorime zdielany adresar
    # chown dev1:developers /repo.d/     <-- nastavime vlastnika/skupinu
    # chmod o-rx /repo.d/                <-- nastavome prava
    # chmod g+s /repo.d/                 <-- nastavime "SGID" bit

 - nasledne overime tak, ze uziv. *dev1* vytvori subor: `$ touch program.c`
 - so spravnym nastavenim ma editovaci pristup aj uzivatel *dev2*

Ako nastavit *Sticky bit*, absolutny mod `$ chmod 1XXX dir1/`, relativny mod `chmod o+t dir1/`
 - zmena zabezpeci, ze sa v (zdielanom) adresary na novy subor *nalepia* prava tvorcu, nie adresara
 - typicky priklad je systemovy adresar `/tmp`, aby si v nom uzivatelia navzajom nemazali subory

Ako nastavovat prava suborov/adresarov napr. v skripte: `$ chmod ug=rw,o=r subor.txt`
 - ako nastavit prava, podla nejakeho vzoroveho suboru: `$ chmod --reference=prvy.txt druhy.txt`

Ako hromadne nastavovat prava suborov, napr.: `$ find $HOME -type f -exec chmod 640 {} \;`

Ako nastavit predvolene prava na vytvorene subory na `0640`, zadame: `$ umask 0026 subor.txt`
 - overime s `$ ls -l subor.txt` alebo `$ stat subor.txt`
 - je dobre si uvedomit, ze pri prikaze `umask` odpocitavame od 0666, teda (0666 - 0026) = 0640
 - pre perzistentne nastavenie vlozime do suborov `.profile` alebo `.bashrc` riadok `umask 0026` 

Pozriet nastroje *eBPF zo sady BCC Tools* a *BPF trace tools*, napr: `$ sudo apt install bpfcc-tools`
 - napr.: `opensnoop-bpfcc`, `execsnoop-bpfcc`, `tcplife-bpfcc`, `ext4slower-bpfcc`, `biosnoop-bpfcc`
 - ohladom disk-IO je este uzitocny nastroj `biotop-bpfcc`
 - dalsie info (kto vie do kedy online): `https://github.com/iovisor/bcc/blob/master/INSTALL.md`
 - dalsie nastroje od Brendana Gregga: `https://brendangregg.com/linuxperf.html`

Typy procesov v operacnom systeme GNU/Linux: `Parent`, `Child`, `Daemon`, `Zombie (defunct)`, `Orphan`

Ako vypisat 3 iteracie programu `top` s oneskorenim 2 s. do suboru: `$ top -d 2 -n 3 -b > stav.txt` 
 
Klavesy v `top` znamenaju: `d` oneskorenie, `e` jednotky RAM, `M` podla RAM, `P` podla CPU, `1` zob. CPU

Ako spustit proces/program, aby ho nezabilo zatvorenie/odpojenie BASH session: `$ nohup <prikaz> &`

Zakladne programy na spravu procesov: `ps`, `pgrep`, `pstree`, `pkill`, `pidof`, `kill`, `killall`
 - dalsie informacie v: `$ man <nazov>`

Ako v systeme  *MacOS - Big Sur* zistit presny typ CPU: `$ sysctl -a | grep brand`

Ako zmenit MAC adresu na Eth. rozhrani: `$ sudo ip link set dev ens33 address 12:34:56:78:9a:bc`

Ako zistit, ake DNS servery pouzivaju distribucie so SystemD: `$ systemd-resolve --status`
 - alebo alternativne: `$ resolvectl status`
 
Ako zadat, uzivatelov, ktori maju povoleny SSH login, do suboru `/etc/ssh/sshd_config` vlozime:

    AllowUsers student1 user1 developer1

 - nasledne upravu ulozime a restartujeme SSH server: `$ sudo systemctl restart ssh`
 - overime s: `$ sudo systemctl status ssh`

Ako overit, ci sa proces/program spusti po restarte systemu: `$ sudo systemctl is-enabled <nazov>`
 - napr.: `$ sudo systemctl is-enabled ssh `

Ako na jednoduchu zalohu adresara `/etc` pomocou `rsync` zadame: `$ sudo # rsync -av /etc/ /media/USBdisk1/zaloha/`

Tip: Tri *divne* sposoby, ako generovat 16 znakove heslo (bez instalacie dalsich programov):
```bash
    $ openssl rand -base64 12
    $ head /dev/urandom | base64 | cut -b 1-16
    $ echo $(head /dev/urandom | shasum | base64 | cut -b 1-11).$(date +%Y)
```
Ako vytvorit/stiahnut kompletnu kopiu/mirror nejakeho webu, pouzijeme program `wget`:

`$ wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.com`
 - alebo skratene: `$ wget -mkEpnp http://example.com`

Ako nainstalovat zakladne vyvojarske nastroje: `$ sudo apt install build-essential`
 - RedHat-based distribucie (Fedora/CentOS) napr.: `$ sudo dnf group install "Development Tools"`

Poznamka: adresar `/opt` znamena *Optional Software*, sluzi zvycajne na kompilaciu programov
 - napr. kompilacia programu `ProFTPD`, pouzijeme nastavenie: `$ ./configure --prefix=/opt/proftpd`

Ako prehladavat lokalnu DPKG databazu (Debu/Ubu): `$ dpkg-query -l | grep ssh`
 - dalej napr. mozeme vypisat obsah balicka: `$ dpkg -L openssh-server`

Ako zistit, do akeho balika patri program `ls`, najskor `$ which ls`, nasledne: `$ dpkg -L /bin/ls`
 - znova mozeme prezriet obsah balika: `$ dpkg -L coreutils | less`
 
Ako overit obsah lokalnej *APT cache* (Deb/Ubu): `$ ls -l /var/cache/apt/archives/`
 - aka je jej velkost: `$ sudo du -sh /var/cache/apt/archives/`
 - mozeme vycistit pomocou: `$ sudo apt clean`

Ako zistit, ake su v systeme nainstalovane baliky: `$ apt list --installed`

Ako vypisat info. o HW pod nainstalovanym systemom: `$ sudo lshw > hw.txt`
 - mozeme vypisat JSON resp. HTML format: `$ sudo lshw -json > hw.json`
   - resp. `$ sudo lshw -html > hw.html`
 - uspornejsi vypis ziskame s: `$ sudo lshw -short`

Podrobne informacie o CPU ziskame s: `$ lscpu`
 - dalej ziskame informacie o RAM: `$ sudo dmidecode -t memory`
 - informacie o velkosti RAM modulov a max. kapacite: `$ sudo dmidecode -t memory | grep -i size`
 - podobne ziskame informacie o zakladnej doske: `$ sudo dmidecode -t baseboard`
 - dalsie moznosti zistime s: `$ sudo dmidecode -t`
 - informacie o zberniciach PCI a USB ziskame s: `$ sudo lspci` resp. `$ sudo lsusb`
 - informacie o HDD/SSD: `$ sudo lshw -C disk`
 - ako ziskat detailne informacie o konkretnom SATA zariadeni: `$ sudo hdparm -I /dev/sda`
 - POZOR, test rychlosti citania SATA, bez cache (raw I/O): `$ sudo hdparm -t --direct /dev/sda`
 - informacie o Wireless zariadeniach ziskame s: `$ sudo iw list | less`
 - ako obvykle, dalsie informacie: `$ man <lshw/lscpu/dmidecode/lspci/lsusb/hdparm/iw>`

Ako zistit kolko trvalo bootovanie pomocou *SystemD*, zadame: `$ systemd-analyze`
 - ak je to mozne, snaha *SystemD* je spustat jednotlive procesy/sluzby *paralelne*
 - da sa detailne vypisat, na com sa travilo najviac casu pri boot-e: `$ systemd-analyze blame`

Ako vypisat *len EXT4-FS* mount-pointy: `$ mount -l -t ext4`
 - dalsi priklad pre VFAT-FS, ktory byva na USB "klucoch": `$ mount -l -t vfat`

Ako vytvorit bitovu kopiu USB disku: `$ sudo dd status=progress if=/dev/sdb of=/home/user1/usb-backup.img`
 - nasledne obnova z image-file: `$ sudo dd status=progress if=/home/user1/usb-backup.img of=/dev/sdb`

Ako vytvorit premennu prostredia (Env. var.) pre cely system, upravime subor `/etc/bash.bashrc`
 - alternativne mozeme pouzit subor `/etc/profile`

Ako zadefinovat *nemennu* konstantu: `$ declare -r nemenna="/var/log"`

Ako v BASH skripte zadefinovat lokalnu (len vo funkcii) premennu: `local var1=len_vo_funkcii`

Ako ulozit vystup zlozeneho prikazu do premennej: `$ output="$(ps -ef | grep ssh)"`
 - nasledne vypiseme (so zachovanym formatovanim) ako retazec/string: `$ echo "$output"`

Ako v BASH skripte testujeme, ze premenna obsahuje substring: `if [[ "$str1" == *[lL]inux"* ]]`

Testovanie BASH premennej s logickymi operatormi: `if [[ $vek -ge 0 ]] && [[ $vek -le 18 ]]`

#### Priklad na cvicny input error handling (osetrenie chybneho vstupu) v jazyku BASH:
```bash
    #!/bin/bash
    #
    # Cvicny skript ocakava cele cislo v ramci vymedzenych hodnot, 17.2.2022 by vlkv
    #
    vek=-1
    set -e
    echo

    while [[ $vek == -1 ]]; do
        read -p "Zadajte vek (rozsah 0 az 120): " vek
            if [[ $vek -le -1 ]] || [[ $vek -ge 120 ]] || ! [[ $vek =~ ^[1-9][0-9]*$ ]]; then
                echo
                echo "CHYBA: Zadany vek \"$vek\" je mimo povolenych hodnot"
                vek=-1
            fi
    done

    echo "Zadali ste vek $vek roky/rokov."

    # koniec skriptu
```
#### Priklad: BASH skript nacita vo `for` slucke hodnoty z `.txt` suboru do premennej `$ip`:
```bash
    #!/bin/bash
    for ip in $(cat /home/dev1/ip_adresy.txt)
    do
        echo "Nacital som zo suboru IP adresu: $ip"
        sleep 1
    done

    # koniec skriptu
```
#### Ako vytvorit skript s jednoduchym *select* menu v jazyku BASH:
```bash
    #!/bin/bash
    #
    #priklad na menu selection v jazyku BASH
    echo
    echo "Zakladna administraciu systemu:"
    echo
    PS3="Zvolte moznost (Enter vypise moznosti): "
    select ITEM in "Pridaj uzivatela" "Vypis procesy" "Zabi proces" "Nainstaluj program" "Koniec"
    do

    	if [[ $REPLY -eq 1 ]]
    	then
    		read -p "Zadajte uzivatelske meno: " username
    		buffer="$(grep -w $username /etc/passwd)"
    		if [[ -n "$buffer"  ]]
    		then
    			echo "Uzivatel \"$username\" uz existuje"
    		else
    			sudo adduser $username
    			if [[ $? -eq 0 ]]
    			then
    				echo "Uzivatel \"$username\" uspesne vytvoreny."
    				tail -n 1 /etc/passwd
    			else
    				echo "Nastala chyba pri vytvarani uzvatela \"$username\""
    			fi
    		fi

    	elif [[ $REPLY -eq 2 ]]
    	then
    		echo "Vypisujem vsetky procesy..."
    		sleep 1
    		ps -ef

            elif [[ $REPLY -eq 3 ]]
    	then
    		read -p "Zadajte nazov procesu: " proces
    		pkill $proces

    	elif [[ $REPLY -eq 4 ]]
    	then
    		read -p "Zadajte nazov balika: " balik
    		sudo apt update && sudo apt install $balik

    	elif [[ $REPLY -eq 5 ]]
    	then
    		echo "Koniec administracie."
    		sleep 1
    		exit

            else
    		echo "Neplatna volba."
            fi
    done

    #koniec skriptu
```
#### Jednoduchy priklad na hladanie substringu zo systemoveho vypisu:
```bash
    #!/bin/bash
    #
    vystup="$(ping -f -i 0.5 -c 3 $1)"

    if [[ "$vystup" == *"100% packet loss"*  ]]
    then
            echo "Internetova konektivita na $1 je nedostupna."
    else
            echo "Konektivita na $1 (ako tak) funguje."
    fi

    # koniec skpritu
```

#### Dalsie zdroje k zakladom BASH skriptov:
 - napr. v knihe: `https://www.root.cz/knihy/bash-ocima-bohdana-milara/`
 - pokrocilejsie skriptovanie, napr. v knihe: `https://tldp.org/LDP/abs/abs-guide.pdf`
 - pripadne pozriet 11. kapitolu v knihe `How Linux Works by Brian Ward, ISBN-13: 9781718500402`

Tip: Ako pomocou jazyka Awk vypisat deviaty stlpec z vypisu: `$ ls -l | awk '{print $9}'`

Pozriet dalsi program na spracovanie textu: `$ man sed`

Pozriet tematiku `BASH Subshell`

#### Praca s prenosom suborov po sieti:

Ako spustit jednoduchy HTTP server (Python modul) v danom adresary: `$ python3 -m http.server`
 - standardne spusteny na TCP porte 8000, mozeme zmenit s: `$ python3 -m http.server 5000`
 - na TCP porty nizsie ako 1024 su potrebne prava `superuser`:
   - prikaz napr.: `$ sudo python3 -m http.server 80`
 - na starsich instalaciach sa da pouzit Python2 modul: `$ python -m SimpleHTTPServer 5000`

Na transfer suborov pomocou programu `rsync`, musi byt program instalovany *na oboch stranach*
 - pre Debian based systemy `$ sudo apt install rsync`
 - alebo pre Fedora Server: `$ sudo dnf install rsync`

Zakladne pouzitie, skopirujeme 3 subory s diagnostikou: 
 - prikaz napr.: `$ rsync -v ifPriklad.sh casePriklad.sh ashow.sh 192.168.1.245:`

Ako kopirovat vsetky adresare `dirX` na stroj s DNS nazvom `ubu2.lab` do adresara `nas`:
 - parameter `-a` umoznuje skopirovat nastavenia suborovych prav, nastavenie UID bitov a pod.
 - teda pouzijeme prikaz: `$ rsync -va dir* ubu2.lab:nas`
 - aby netrebalo zadavat SSH heslo, moze nahrat verejny kluc PKI: `$ ssh-copy-id userXYZ@ubu2.lab`
 - ked chceme transfer/zalohu len otestovat, pouzijeme parameter `-n`:
   - prikaz: `$ rsync -n -va dir* ubu2.lab:nas`

*POZOR*, ak chceme v cieli vytvorit *EXAKTNU* kopiu lokalneho(ych) adresara(ov), ktora *ZMAZE* nove subory v cieli:

 - pouzijeme: `$ rsync -va --delete dir* ubu2.lab:nas`
 - diagnosticky parameter `-v` vypise, ktore subory v cieli boli vymazane

Ak chceme kopirovat *LEN* obsah lokalneho adresara po sieti, pouzijeme dolezity znak `/`:
 - prikaz: `$ rsync -av dir1/ ubu2.lab:`

Ked chceme vynechat subor, specifikujeme absolutnu cestu: 
 - prikaz: `$ rsync -av --exclude=dir1/junk.txt dir1 ubu2.lab:`

Ked chceme prenos overit kontrolnym suctom, pouzijeme parameter `-c` alebo `--checksum`

Pozriet v `$ man 1 rsync` dalsie parametre ohladom zalohovania: `-b`, `--suffix=.old` a `-u` 

Ako obmedzit Bandwidth prenosu, napr. na *50MBytes/s* (cca 400Mbit/s):
 - prikaz: `$ rsync -a --bwlimit=50000 same_nuly.txt ubu2.lab:`
 - priklad ako vytvorit testovaci 1GiB subor: `$ dd if=/dev/zero of=same_nuly.txt bs=1024 count=1M`
 
Poznamka: pozriet dokumentaciu a manualy k projektu *Samba File/Printer Sharing*
 - tento projekt nie je predmetom certifikacnej skusky

#### Praca s projektom SSHFS - SSH File System:

Ako si pripojit vzdialny adresar cez SSH, napr.: `$ sshfs userABC@ubu2.lab:/mnt/lvnas1 sshnas.d/`
 - kombinovatelne s PKI auth (prihlasovanie verejnym klucom)
 - ako vykonat u-mount pripojeneho disku: `$ fusermount -u sshnas.d/`

#### Praca s premennymi prostredia v interprete BASH:

Premenne prostredia pre interpret BASH su definovane v *skrytych* suboroch: `.bash_profile` alebo `.profile`

- priklad na definiciu premennej shellu: `$ TEST=123`
- priklad na definiciu premennej prostredia: `$ export TESTENV=567`

Dolezite adresare na spustanie binarnych aplikacii a skriptov su ulozene v premennej `$PATH`

- zvycajne sa jedna o adresare: `/usr/local/bin`, `/usr/bin` a `/bin`
- overime s prikazom: `$ echo $PATH`

Tip: V definicii promptu, teda v premennej `$PS1` by sme sa mali vyhnut znakom: `{ } = & < >`
 - dalsie detaily najdeme v manualy, v sekcii `PROMPTING` vid.: `$ man bash`

### Zaklady prace s vyvojarskymi nastrojmi:

#### Jednoduchy priklad ako kompilovat zdrojove subory v jazyku *C*:
- vytvorime zdrojovy subor `pokus.c`, kde vlozime prikazy:
```c
    #include <stdio.h>

    int main(void) {

        printf("Hello, World.\n");
    }
```

- nasledne skompilujeme, treba nainstalovat dev. nastroje: `$ sudo apt install build-essential`
- na kompilaciu pouzijeme program `cc`, teda "C Compiler": `$ cc pokus.c`
- vystupom bude spustitelny binarny subor `a.out`, spustime: `$ ./a.out`
- pri kompilacii mozeme specifikovat nazov vystupneho suboru: `$ cc -o pokus pokus.c`

Tip: Ako vypisat zdielane kniznice, ktore ma nalinkovane dany program: `$ sudo ldd /usr/bin/bash`

#### Jednoduchy priklad ako kompilovat zdrojove subory v jazyku *Java*:

Je potrebne nainstalovat vyvojarske nastroje: `$ sudo apt install default-jdk-headless`

Vytvorime jednoduchy cvicny zdrojovy subor `pokus.java`:
```java
    class MyFirstProgram {

        public static void main(String args[]){
            System.out.println("Hello World!");
        }
    }
```

 - program skompilujeme do tzv. *byte code* formatu s priponou `.class`: `$ javac pokus.java`
 - vznikne bytecode subor `MyFirstProgram.class`, ktory spustime prikazom: `$ java MyFirstProgram`

#### Ako kompilovat a instalovat distribuovane zdrojove baliky:
 - na test si vytvorime adresar `test_coreutils` prikazom: `$ mkdir test_coreutils`
 - do vytvoreneho adresara stiahneme zdrojovy balik:
   - prikaz: `$ wget https://ftp.gnu.org/gnu/coreutils/coreutils-9.0.tar.gz`
 - rozbalime zdrojovy archiv: `$ tar -xvzf coreutils-9.0.tar.gz`
 - v rozbalenom adresary `coreutils-9.0` spustime konfiguracny *GNU Autoconf* skript `configure`
 - tento skript konfiguruje parametre kompilacie a naslednej instalacie
 - skript spustime s parametrom cieloveho adresara kompilacie a instalacie: 
   - prikaz: `$ ./configure --prefix=$HOME/test_coreutils`
 - nasledne po konfiguracii spustime v danom adresary kompilaciu: `$ make`
 - skompilovane programy a binarne objekty najdeme v adresary `coreutils-9.0/src/`
 - po kompilacii mozeme spustit rozsiahle overenie kompilacie: `$ make check`
 - po kompilacii mozeme *na sucho/dry run* spustit test instalacie: `$ make -n install`
 - po overeni mozeme spustit samotnu instalaciu: `$ make install`
 - po instalacii v adresary `test_coreutils` vzniknu adresare `bin`, `libexec`, `share`
 - na Debian-based distr. je nastroj na nastavenie parametrov `.deb` balickov `checkinstall`:
   - prikaz: `$ sudo apt install checkinstall`
 - *POZOR* na testovacej instalacii sa da spustit tvorba balicka: `$ sudo checkinstall make install`
 - hore uvedenym prikazom sa da rozbit system, tak si treba na test VM spravit *snapshot/backup*

### Zaklady prace s virtualnymi kontajnermi, projekt Docker:

Instalacia najznamejsieho nastroja Docker nie je zlozita, ale ani trivialna, jeden z postupov:

`https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04`

Ako otestovat instalaciu Docker-a a jeho pripojenie na Docker Hub: `$ docker run hello-world`

Na zakladne vytvorenie Docker kontajneru je potrebne definovat Docker file s nazvom `Dockerfile`

Tento Docker file je vhodne umiestnit do oddeleneho adresara.

Obsah suboru moze byt podla jednoducheho prikladu, kedy definujeme kontajner systemu Alpine Linux:

    FROM alpine:latest
    RUN apk add bash
    CMD ["/bin/bash"]

- po ulozeni suboru mozeme zostavit image nasledovne: `$ docker build -t alpine_test1 .`

#### Zakladne prikazy pre nastroj Docker:

Ako vypisat zakladne informacie o instalacii Docker a o systeme, na ktorom bezi: `$ docker info`

Ako vypisat vytvorene Docker image: `$ docker images`

Ako spustit kontajner (z image) a pripojit sa na jeho "konzolu": `$ docker run -it alpine_test1`

Ako sledovat aktualnu alokaciu zdrojov: `$ docker stats`

Ako vypisat zoznam aktivnych kontajnerov: `$ docker ps`

Ako vypisat aktivne aj neaktivne kontajnery: `$ docker ps -a`

Ako vypisat posledny vytvoreny kontajner: `$ docker ps -l`

Ako zmazat neaktivny kontajner: `$ docker rm <ID/nazov>`

Ako zmazat Docker image: `$ docker rmi <ID/nazov image>`

Ako hladat image na Docker Hub-e: `$ docker search ubuntu`

Ako stiahnut image z Docker Hub-u: `$ docker pull ubuntu`

Ako zastavit kontajner: `$ docker stop <ID/nazov>`

Ako spustit zastaveny kontajner: `$ docker start <ID/nazov>`

Ako sa pripojit na "kozolu" kontajneru, ktory bezi: `$ docker attach <ID/nazov>`

Ako sa odpojit od konzoly kontajnera, v terminale za sebou stlacime skratky: `Ctrl+p` a `Ctrl+q`

#### Dalsie poznamky k praci s Docker-om:

Jednoduche web prostredie na ucenie/testovanie Docker-u: `https://labs.play-with-docker.com/`
 - dalsie informacie: `https://www.docker.com/play-with-docker`

Priklad ako spustit v *sandboxe* prostredi web server `nginx`, zadame: `$ docker container run -d -it nginx`

Pre pomoc s CLI, staci zadat prikaz bez parametrov, napr.: `$ docker container`

Priklad ako vytvorit zmenu v Docker image a commitovat ju:
- zadame : `$ docker commit -m "pridany nmap" -a "Jan Novak" <cont-ID> <hub-repoID>/moje-ubu:latest`

 - nasledne overime s: `$ docker image ls`
 - mozeme napr. z noveho image spustit container s: `$ docker container run -it ddnovak/moje-ubu`

*POZOR*, prikaz vymaze *vsetky nebeziace* kontajnery: 
 - prikaz: `$ docker container rm $(docker container ls -a -q)`
 - pripadne na *VLASTNE RIZIKO* mozeme spustit s paramentrom: `rm -f`

Ako spustit testovaci webserver v kontajnery s nazvom `moj_lab` (vonkajsi port je *TCP/8080*):

prikaz: `$ docker container run -d -p 8080:80 --name=moj_lab nginx`

 - overime s: `$ docker ps`
 - nasledne otestujeme pripojenie s browserom, alebo napr. `$ curl localhost:8080`
 - dalsie informacie: `$ docker container run --help`
 - alternativne, image s web serverom Apache2, nazov image zmenime na: `httpd`

Ako vypisat otvorene TCP porty kontajnera: `$ docker container port <contID/contNAME>`

Ako vypisat logy z kontajnera (napr. server nginx): `$ docker container logs <contID/contNAME>`
 - sledovanie v realnom case, doplnime parameter: `logs -f`

Ako sledovat zdroje konkretneho kontajnera: `$ docker container stats <contID/contNAME>`

Ako vypisat detailne informacie o kontajnery: `$ docker container inspect <contID/contNAME>`

Ako spustit kontajner, hned s prikazovym riadkom: 

prikaz: `$ docker container run --name=ubu-con1 -it ubuntu`
 - alebo, spustime interaktivny BASH na uz vytvorenom kontajnery: `$ docker exec -it ubu-con1 bash`
 - alebo, spustime (zastaveny) kontajner v interaktivnom mode: `$ docker start -i ubu-con1`

Ako vypisat kolko miesta na disku zaberaju kontajnery: `$ docker ps -as`

Ako vytvorit perzistentne ulozisko pre kontajner *Docker Volume*: `$ docker volume create <nazov>`
 - overime s `$ docker volume ls`
 - dalsie informacie: `$ docker volume --help`

Ako vytvorit *nginx* kontajner s namapovanyn uloziskom *volume*:

prikaz: `$ docker run -d --name moja_web_app -p 80:80 -v <nazov_vol>:/usr/share/nginx/html nginx`
 
- mozeme manipulovat s obsahom *web root* adresara v: `/var/lib/docker/volumes/mojvol/_data/`
- priklad: `$ sudo cp /etc/services /var/lib/docker/volumes/mojvol/_data/index.html`
- overime napr. s: `$ curl localhost:80`

Poznamka: ak chceme vymazat Docker image, treba najskor pomazat z neho vytvorene kontajnery.

*POZOR*, automaticky nastroj na cistenie tzv. *dangling* Docker image-ov: `$ docker system prune`
 - dalsie informacie: `$ docker system prune --help`
 - celkom uzitocna diagnostika zabrateho miesta: `$ docker system df`

### Zaklady prace s nastrojom Git a platformou GitHub:

Vytvorime adresar `git_ucenie`, v ktorom inicializujeme *lokalny* Git repozitar: `$ git init`
 - aktualny stav repozitara overime s: `$ git status`
 - nastavime identitu uzivatela na pridavanie zmien: `$ git config --global --edit`
 - vytvorime cvicny subor, napr. `poznamky.txt`
   - do suboru napiseme `moja prva poznamka`, subor ulozime
 - nasledne subor pridame do *Staging Cache* repozitara: `$ git add poznamky.txt`
 - overime s: `$ git status`
 - dalej pridame do *lokalneho* repozitara novu zmenu, teda *commit* s popisom/spravou: 

   - prikaz: `$ git commit -m 'vytvoril som subor poznamky.txt a pridal 1. riadok'`

 - dalej upravime subor `poznamky.txt`, pridame riadok `dalsi riadok s poznamkou`
 - subor ulozime a overime stav *lokalneho* repo.: `$ git status`
 - podla vypisu je potrebne pridat upraveny subor do *Staging Cache*: `$ git add poznamky.txt`
 - jednoduchsie mozeme pridat vsetky subory v danom adresary repozitara: `$ git add .`
 - aby sme sa vyhli pridavaniu suborov, ktore nechceme pridat do Staging Cache, vytvorime subor `.gitignore`
 - na ignorovanie tzv. *.dotfiles* mozeme do suboru zapisat napr. riadok `.*`
 - ak chceme odstranit subor z Cache, pouzijeme: `$ git rm --cached <nazov_suboru>`
 - pridame novu zmenu: `$ git commit -m 'pridal som dalsi riadok'`

Chceme napr. zmenit format zapisu poznamok, mozeme vytvorit novu "vetvu", tzv. *branch*:
 - prikaz:  `$ git checkout -b 'novy_format'`
 - v novej vetve napr. vytvorime subor `poznamky_novy_format.txt` a ten pridat do Cache a commit-ovat
   - avsak uz do *novej vetvy/branch* s nazvom `novy_format`
 - overime s: `$ git status`
 - potom sa mozeme prepinat medzi vetvami, napr. sa vratit do hlavnej *master* vetvy:
   - prikaz: `$ git checkout master`
 - overime s: `$ git status`

#### Ako replikovat lokalny Git repozitar na vzdialeny server, napr. na GitHub:

- na platforme `github.com` si vytvorime uzivatelsky ucet
- je potrebne vytvorit si autentifikacny Token, tzv. *PAT - Personal Access Token*, podla odkazu:

`https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token`

- vytvoreny Token *nezabudame/nezatvarame*
- dalej vytvorime repozitar s nazvom `git_ucenie`, portal *GitHub* nam vygeneruje zakladne prikazy
- dalej si vytvorime vzdialeny pristup na repo., tzv. *Remote*: 
  - prikaz: `$ git remote add origin https://github.com/<UZIVATEL>/git_ucenie.git`
- nasledne zosynchronizujeme kolakny repo. so vzdialenym repo.: `$ git push -u origin master`
- na autentifikaciu zadame svoje uzivatelske meno, ale *namiesto hesla zadame vygenerovany PAT token*

Na ulahcenie prace s Git-om mozeme pridat do svojho `$HOME` adresara, do suboru `.gitconfig` aliasy, napr.:

    #
    [alias]
        s = status
        co = checkout
        cob = checkout -b
        save = !git add -A && git commit -m 'Nic zasadne: len ukladam pripisany text'
        lg = !git log --pretty=format:\"%C(magenta)%h%Creset -%C(red)%d%Creset %s %C(dim green)(%cr) [%an]\" --abbrev-commit -30
        undo = reset HEAD~1 --mixed
        strom = !git log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C$

Naslendne uz mozeme pouzivat napr. tieto aliasy:

    $ git s
    $ git save
    $ git lg
    $ git strom

### Zaklady bezpecnosti v operacnom systeme GNU/Linux:
Poznamka: dva webove zdroje s informaciami k typom a kategoriam utokov:
```
https://www.nsa.gov/Press-Room/Cybersecurity-Advisories-Guidance/

https://attack.mitre.org/
```

#### Nastroj na ochranu/kontrolu integrity suborov a adresarov, projekt *AIDE*:
Instalacia pre Debian-based systemy: `$ sudo apt install aide`
 
 - instalacia v systeme Fedora Server: `$ sudo dnf install aide`
 - dalsie informacie: `https://aide.github.io/`
 - vypiseme verziu a skompilovane moduly: `$ aide -v`
 - dalej mozeme vypisat moznosti a parametre: `$ aide --help`
 - konfiguracny subor je ulozeny v `/etc/aide/aide.conf`
 - inicializujeme *AIDE*: `$ sudo aideinit`
 - inicializacia Fedora Server: `$ sudo aide -i`
 - prikaz bezi nejaku dobu a vytvori (na Ubu) *databazu signatur* v: `/var/lib/aide/aide.db.new`
 - databa na Fedora Server: `/var/lib/aide/aide.db.new.gz`
 - dalej sa venujem *AIDE* na *Ubuntu*:
 - po vytvoreni DB je potrebne nahradit povodnu DB novou: `$ sudo mv aide.db.new aide.db`
 - na test mozeme spravit napr. zmeny v adresary `/root` alebo pridat uzivatela: `$ sudo useradd X`
 - overime zmeny: `$ sudo aide -c /var/lib/aide/aide.conf.autogenerated --check > aide.report.txt`
 - nasledne pozrieme zmeny: `$ sudo less aide.report.txt`
 - je vhodne znova aktualizovat DB: `$ sudo aide -c /var/lib/aide/aide.conf.autogenerated --update`
 - dalej je potrebna nahrada: `$ sudo mv aide.db.new aide.db`
 - vykonane zmeny v konfiguraci `/etc/aide/aide.conf` treba aplikovat: `$ sudo update-aide.conf`
 - priklad zmeny na `SHA256`, riadok `Checksums = sha256+sha512+rmd160+haval+gost+crc32+tiger`
   - zmenime na `Checksums = sha256` cim dosiahneme zrychlenie, pokial nam postacuje len `SHA256`
   - mozeme nastavit ignorovanie niektorych adresarov/suborov, do konf. pridame riadok:

     `!/var/lib/aide/.*`

 - a nasledne inicializujeme s novou databazou: `$ sudo aideinit`
 - dalej je mozne vytvorit si vlastny config a vlastne pravidla, navody existuju ;-)

#### Na overovanie bezpecnosti hesla mozeme pouzit nastroj *John the Ripper*:
 - instalacia na Ubu/Deb: `$ sudo apt install john`
 - zlucime `/etc/passwd` a `/etc/shadow` prikazom: `$ sudo unshadow /etc/passwd /etc/shadow > unshadow.out.txt`
 - na test spustime jednoduchy *single mode*, zadame : `$ sudo john -single unshadow.out.txt`
 - overime s: `$ sudo john --show unshadow.out.txt`
 - vysledok pozrieme ulozeny v: `$ sudo less /root/.john/john.pot`
 - slovnikovy utok: `$ sudo john --wordlist=/usr/share/john/password.lst --rule unshadow.out.txt`
   - stlacenim napr. *medzernika* ziskame *stav* priebehu
   - stlacenim `Ctrl+c` alebo `q` prerusime prelamovanie, ale nestratime priebeh
   - priebezne vysledky ziskame s: `$ sudo john --show unshadow.out.txt`
   - prelamovanie mozeme obnovit s: `$ sudo john -restore`

Politiku systemovyh hesiel najdeme v subore `/etc/login.defs`
 - dalsie informacie v: `$ man login.defs`

Ako nastavit cas expiracie hesla na 30 dni: `$ sudo chage -M 30 <uzivatel>`
 - overime s: `$ sudo chage -l <uzivatel>`

#### Dalsie politiky hesla, napr. jeho zlozitost spravuju *PAM - Pluggable Authentification Modules*:
 - treba instalovat balik: `$ sudo apt install libpam-pwquality`
 - konfiguracia v subore: `/etc/pam.d/common-password`
 - na upravu politiky pridame do riadku `password requisite pam_pwquality.so retry=3`
   - mozeme pridat aj dalsie atributy:

    `minlen=10 difok=3 ucredit=-1 lcredit=-1 dcredit=-1 ocredit=-1`

 - kde jednotlive atributy znamenaju:
   - `retry=` kolko krat sa login process spyta na heslo 
   - `minlen=` minimalna dzlka hesla
   - `difok=` minimalny pocet znakov odlisnych od povodneho hesla
   - `ucredit=` atribut s `-1` vyzaduje aspon jedno velke pismeno (upper case)
   - `lcredit=` atribut s `-1` vyzaduje aspon jedno male pismeno (lower cace)
   - `dcredit=` atribut s `-1` vyzaduje aspon jeden numericky znak (numeric character)
   - `ocredit=` atribut s `-1` vyzaduje aspon jeden specialny znak (special character)
   - na *RedHat-based* distribuciach sa pouziva konf. subor: `/etc/pam.d/system-auth`

#### Ako vytvorit sifrovanu particiu na HDD/SSD
- je potrebne nainstalovat: `$ sudo apt install cryptsetup`
 - disk, ktory chceme sifrovat, musi byt v stave *unmounted*
 - dalej spustime sifrovanie a nastavime kluc/heslo: `$ sudo cryptsetup -y -v luksFormat /dev/sdX`
 - nasledne vytvorime mapovacie zariadenie: `$ sudo cryptsetup luksOpen /dev/sdb crypt1`
   - vytvori sa symbolicky link `/dev/mapper/crypt1 -> /dev/dm-X`
 - overime s: `$ sudo cryptsetup status crypt1`
 - po overeni vytvorime particu/FS, napr. Ext4: `$ sudo mkfs.ext4 /dev/mapper/crypt1`
 - dalej *namountujeme* novu particiu na adresar: `$ sudo mount /dev/mapper/crypt1 /mnt/crypt1/`
 - volitelne nastavime vlastnika/prava, napr.: `$ sudo chown user1:user1 /mnt/crypt1/`
 - po ukonceni prace: `$ sudo umount /mnt/crypt1` nasledne: `$ sudo cryptsetup luksClose crypt1`
 - nova uloha: `$ sudo cryptsetup luksOpen /dev/sdb crypt1`
   - nasledne: `$ sudo mount /dev/mapper/crypt1 /mnt/crypt1/`

#### Zaklady prace s nastrojom `sudo`: 
 - relacia vytvorena prikazom `sudo` ma pristupove prava v `cache` presne 15 min
 - cache sa da zmanzat s: `$ sudo -k`
 - toto nastavenie mozeme zmenit, napr. na 10 min., otvorime konfiguraciu `sudoers`, zadame: `$ sudo visudo`
 - nasledne riadok `Defaults env_reset` upravime na: `Defaults env_reset, timestamp_timeout=10` 
 - mozeme nadefinovat povolene prikazy, dopiseme: `user1  ALL=(root)      /usr/bin/ls,/usr/bin/cat`
 - na zjednodusenie definujeme aliasy, priklad v subore `/etc/sudoers` moze cast vyzerat takto:
   - vytvorime alias uzivatelov *ADMINS* v ktorom su 3 uziv., dalej alias na prikazy *FILE_OPER*

Aliasu `ADMINS` priradime povoleny prikaz `/user/bin/netstat` + alias prikazov `FILE_OPER`:

    # User alias specification
    User_Alias ADMINS=user1,user2,dev1

    # Cmnd alias specification
    Cmnd_Alias FILE_OPER=/usr/bin/cp,/usr/bin/ls/,/usr/bin/touch/,/usr/bin/rm

    # User privilege specification
    root    ALL=(ALL:ALL) ALL
    ADMINS  ALL=(root)      /usr/bin/netstat,FILE_OPER

 - dalsie informacie: `$ man sudoers`

#### V oblasti *Steganografie* sa pouziva nastroj `steghide`:
 - instalujeme: `$ sudo apt install steghide`
 - dalsie informacie: `https://en.wikipedia.org/wiki/Steganography`
 - informacie o programe: `$ man steghide`

#### Dalsie priklady prace s uzivatelskymi uctami:
Ako docasne deaktivovat *password-auth* pre daneho uzivatela: `$ sudo passwd -l <uzivatel>`
 - overime s: `$ sudo passwd --status <uzivatel>`
   - vo vypise znak `L` znamena *Locked*, dalej `P` = Valid Password, `NP` = No Password
 - uzivatleske heslo znova *odomkneme* s: `$ sudo passwd -u <uzivatel>`
 - overime s: `$ sudo passwd --status <uzivatel>`
 - dalsi psosob zamknutia, zmena datumu exspiracie hesla: `$ sudo usermod --expiredate 1 <uzivatel>`
 - overime s: `$ sudo chage -l <uzivatel>`
 - znova *aktivujeme* s: `$ sudo usermod --expiredate "" <uzivatel>`

#### Zaklady prace s programom `nmap`:
Ako s Nmap TCP skenovanim "odhadnut" verziu OS a programov: `$ sudo nmap -A -Pn -sV 192.168.1.100`
 - parameter `-Pn` zabezpeci, ze sa nepouzije *ping-check*, nmap pokracuje aj ked sa ICMP pakety zahadzuju
 - *SEDA ZONA*, mozeme pouzit tzv. *Decoys*, napr.: `$ sudo nmap 192.168.1.2 -D A.B.C.D,E.F.G.H,I.J.K.L`
   - tieto Decoy hosty musia byt *UP*
 - sken bez prekladu PTR `-n`, zo zoznamu `-iL hosts.txt`, vystup ide do suboru `-oN output.txt`:
   - napr: `$ sudo nmap -sV -iL hosts.txt -n -oN output.txt`
 - program `nmap` pouziva koncept *Templates*, dalsie info v `$ man nmap`, vyhladat parameter: `-T`

#### Nastroje na detekciu tzv. *Rootkit-ov*:
 - instalujeme: `$ sudo apt install rkhunter`
 - nasledne aktualizujeme *file-DB*, zadame: `$ sudo rkhunter --propupd`
 - dalej spustime samotne skenovanie: `$ sudo rkhunter --check`
 - vysledok mozeme skontrolovat s: `$ sudo less /var/log/rkhunter.log`
 - mozeme spustit len *Warning* reportovanie: `$ sudo rkhunter --check --report-warnings-only`
   - log sa da stale sledovat, napr.: `$ sudo tail -f /var/log/rkhunter.log`
   - mozeme naist `False-positives`, da sa pridat do `/etc/rkhunter.conf`, co chceme ignorovat:
   - pridame napr. riadok: `SCRIPTWHITELIST=/usr/bin/lwp-request`
   - lepsie riesenie moze byt specifikovanie *Package* manazera, pridame: `PKGMGR=DPKG`

Dalsi nastroj na *Rootkit* detekciu je `chkrootkit`
 - instalujeme s: `$ sudo apt install chkrootkit`
 - jednoduche spustenie: `$ sudo chkrootkit`
   - podobne sa da spustit, len vypise *Warnings*, prikaz: `$ sudo chkrootkit -q`

#### Ako hladat/mazat virusy, pouzijeme projekt *Clam-AV*:
 - instalujeme: `$ sudo apt install clamav clamav-daemon`
 - dolezite komponenty: `$ man clamd`, `$ man clamdscan`, `$ man clamscan` (pouziva vlastnu *Virus-DB*)
 - nastroj na aktualizaciu *Virus-DB*, informacie: `$ man freshclam`
 - aktivnu aktualizaciu overime s: `$ sudo systemctl status clamav-freshclam`
 - verziu DB overime s: `$ freshclam --version`
 - dalej mozeme spustit Clam-AV process: `$ sudo systemctl start clamav-daemon`
   - *POZOR*, moze byt narocne na RAM (u mna cca. 1,2 GB)
 - overime stav s: `$ sudo systemctl status clamav-daemon`
   - ak chceme, aby proces startoval *on-boot*, tak: `$ sudo systemctl enable clamav-daemon`
 - overime aj log, napr.: `$ sudo less /var/log/clamav/clamav.log`
 - mozeme stiahnut testovaci virus: `$ wget -c www.eicar.org/download/eicar.com`
   - nasledne testovaci sken: `$ sudo clamdscan --fdpass /home`
   - najdene subory mozeme presunut do karanteny: `$ sudo clamdscan --move /karantena --fdpass /home`
   - *POZOR*, na vlastne riziko mozeme aj mazat: `$ sudo clamdscan --remove --fdpass /home`
 - mozeme pouzit nastroj `clamscan`, ktory si nacita vlastnu DB:
   - najskor zastavime *ClamAV-Daemon*, prikaz: `$ sudo systemctl stop clamav-daemon`
   - nasledne spustime skenovanie: `$ sudo clamscan --recursive /home`
   - upravime vypis, aby zobrazil *nakazene* subory: `$ sudo clamscan --infected --recursive /home`
   - *POZOR*, automaticke mazanie: `$ sudo clamscan --infected --remove --recursive /home`
   - pre Linux-ove distribucie existuje aj GUI rozhranie *ClamTk*, instalujeme: `$ sudo apt install clamtk`

#### Ako na zabezpecnie zavadzaca *GRUB2*:
 - vytvorime heslo: `$ sudo grub-mkpasswd-pbkdf2`
 - dalej upravime subor `/etc/grub.d/40_custom` pridame riadky, vygenerovany HASH, od slova `grub`
```
 set superusers="root"
 password_pbkdf2 root grub.pbkdf2.sha512.10000.C319ED4060EA...
```

 - nasledne ulozime a spustime skript na generovanie konfiguracie: `$ sudo update-grub2`

#### Zabezpecenie servera *OpenSSH*:
- hlavna konfiguracia je ulozena v subore: `/etc/ssh/sshd_config`
- rozsiahly zdroj informacii: `$ man sshd_config`
- zvazit zmenu pocuvajuceho TCP portu, upravime riadok `#Port 22` na `Port 5022`
- po zmenach je potrebne: `$ sudo systemctl restart ssh`
- overime s: `$ sudo systemctl status ssh`
- deaktivujeme *root-login*, teda zmena: `#PermitRootLogin prohibit-password` na `#PermitRootLogin no`
- odpoji po 5 min. neaktivity, pridame 2 riadky `ClientAliveInterval 300` a `ClientAliveCountMax 0`
- maximalny pocet pokusov pri zadavani hesla, zmenime: `#MaxAuthTries 6` na `MaxAuthTries 3`
- dalej pozriet v `$ man sshd_config` parametre: `MaxStartups` a `LoginGracetime`

#### Ako zabranit tzv. *Fork bomb-am*:
- je potrebne overit pocet spustitelnych procesov, skontrolujeme povolnene mznostvo: `$ ulimit -u`
- do suboru `/etc/security/limits.conf` pridame tieto riadky:
    ```
    student		hard	nproc	1000
    @team1		hard	nproc	4000
    ```
 - prvy riadok obmedzi pocet procesov pre daneho uzivatela, druhy pre danu skupinu
 - *POZOR, LEN MIMO PRODUKCIE*, priklad na BASH fork-bomb, vytvorime skript s riadkom `$0 && $0 &`
   - skript do "nekonecna" spusta kopie sameho seba, kym nevycerpa systemove zdroje
   - *POZOR*, priklad Fork bomby vo forme prikazu: `$ :(){ :|:& };:`
   - prikaz na overenie, kolko procesov ma spusteny uzivatel: `$ pgrep -wcu <uzivatel>`
 - dalej mozeme obmedzit max. velkost suboru (v kB), ktory moze uziv. vytvorit:
```
    student		hard	fsize	1000
```
 - dalsie informacie napr. v: `$ man limits.conf`

#### Ako zasifrovat subor s citlivymi udajmi pomocou projektu *GNU-PG*:
- prikaz: `$ gpg -c povodny.txt`
- vznikne sifrovany subor `povodny.txt.gpg`, ktory napr. premenujeme na `sprava.dat` a posleme
- mozeme aj upresnit sifru a vystup: `$ gpg -c --cipher-algo aes256 -o sprava.dat povodny.txt`
- *OPATRNE*, ak treba, mozeme spolahlivo *znicit* povodny subor: `$ shred -uv -n 100 povodny.txt`
- v cieli sa subor desifruje: `$ gpg -o povodny.txt -d sprava.dat`
- dalsie informacie napr. v: `$ man gpg` alebo `$ gpg --help`

### Zaklady prace s DNS serverom BIND 9:
- instalujeme: `$ sudo apt install bind9 bind9-utils bind9-doc`
- dalsie implementacie autoritativnych DNS serverov: `Knot DNS`, `DNSmasq`, `PowerDNS`, ...
- standardna `bind9` Ubu/Deb instalacia spusti *Cache-only* server, pocuva na IPv4 aj IPv6
- ak to chceme zmenit, upravime `/etc/default/named`, do riadku `OPTIONS="-u bind"`, pridame parameter `-4` alebo `-6`, vzajomne sa vylucuju
- hlavna konfiguracia DNS servera *BIND9* je v subore `/etc/bind/named.conf`
- ked chceme pridat tzv. *forwarder* servery, pridame do `/etc/bind/named.conf.options` riadky:

```bind
    forwarders {
                    193.17.47.1;
                    185.43.135.1;
                    2001:148f:ffff::1;
                    2001:148f:fffe::1;
            };
```
- poznamka: ako priklad som pouzil ODVR servery NIC.cz: `https://www.nic.cz/odvr/`
- nasledne restartujeme proces/daemon servera: `$ sudo systemctl reload-or-restart bind9.service`
- stav mozeme overit s: `$ sudo systemctl status bind9.service`

Tip: Ako zistit, ake NS servery pouziva dana domena: `$ dig -t ns example.com`

Ako pridat domenu/zonovy subor, tzv. *zone-file*, teda vytvorit autoritaivny DNS server pre domenu:
 - do suboru `/etc/bind/named.config.local` pridame riadky:
```named
    zone "priklad.xyz" {
    	type master;
    	file "/etc/bind/db.priklad.xyz";
    };
```
 - nasledne si zo sablony skopirujeme zonovy subor `/etc/bind/db.priklad.xyz`
   - prikaz: `$ sudo cp /etc/bind/db.empty /etc/bind/db.priklad.xyz`
 - tento subor upravime napr. nasledovne:
```named
    ;
    ; Priklad na zonovy subor domeny "priklad.xyz"
    ;
    $TTL	86400
    @	IN	SOA	ns1.priklad.xyz root.localhost. (
    			      2		; Serial
    			 604800		; Refresh
    			  86400		; Retry
    			2419200		; Expire
    			  86400 )	; Negative Cache TTL
    ;
    @	    IN	NS	ns1.priklad.xyz
    @	    IN	NS	ns2.priklad.xyz
    ns1	    IN	A	192.168.1.244
    ns2	    IN	A	192.168.1.242
    mail	IN	MX 10	mail.priklad.xyz.
    priklad.xyz.	IN	A	192.168.1.244
    www	    IN	A	192.168.1.244
    mail    IN	A	192.168.1.244
```
 - dalej je vhodne otestovat spravnost konfiguracie servera a zonovych suborov:
   - kontrola konf. servera: `$ sudo named-checkconf`
   - kontrola zonoveho suboru: `$ sudo named-checkzone priklad.xyz. /etc/bind/db.priklad.xyz`
 - po kontrole restartujeme DNS server: `$ sudo systemctl reload-or-restart bind9.service`
 - stav overime s: `$ sudo systemctl status bind9.service`

Tip: Ako zistit, svoju verejnu IP, napr.: `$ curl ifconfig.me`, `$ curl -4 ident.me`, `$ curl -6 ident.me`
 - priklad, pouzitie v skripte: `$ echo "Moja verejne IP je $(curl -s ident.me)"`

### Zaklady prace s webovym serverom Apache2:

#### Ako zadefinovat tzv. *Virtual Hosting* pre Web server Apache2:

 - vytvorime adresar s webom: `$ sudo mkdir /var/www/priklad.xyz`
 - nastavime vlastnika: `$ sudo chown -R www-data:www-data /var/www/priklad.xyz`
 - nastavime prava: `$ sudo chmod 755 /var/www/priklad.xyz`
 - vytvorime konf. subor: `$ sudo vim /etc/apache2/sites-available/priklad.xyz.conf`
 - vlozime napr.:
```apache
    <VirtualHost *:80>
        ServerName priklad.xyz
        ServerAlias www.priklad.xyz
        DocumentRoot "/var/www/priklad.xyz"

        ServerAdmin web@priklad.xyz
        ErrorLog /var/log/apache2/priklad.xyz.error.log
        CustomLog /var/log/apache2/priklad.xyz.access.log combined

    </VirtualHost>
```
 - po ulozeni aktivujeme a pridame stranku do *Virtual Hosting* s: `$ sudo a2ensite priklad.xyz`
 - vznikne: `/etc/apache2/sites-available/vlkv.name.conf -> /etc/apache2/sites-enabled/vlkv.name.conf`
 - nasledne znova nacitame konfiguracie servera: `$ sudo systemctl reload apache2`
 - mozeme overit s: `$ sudo systemctl status apache2`
 - mozeme aj deaktivovat ine *Virtual Host* stranky
 - napr. deaktivujeme predvolenu *Landing Page* pre Apache2 na Debiane: `$ sudo a2dissite 000-default`
 - je este potrebne znova nacitat konfigy: `$ sudo systemctl reload apache2`

#### Ako nainstalovat podporu PHP na server Apache2:
 - instalujeme baliky: `$ apt install php php-mysql libapache2-mod-php`
 - instalaciu overime napr. s: `$ php -v`
 - na otestovanie vo Web prehliadaci mozeme vytvorit jednoduchu stranku
   - v adresari `/var/www/priklad.xyz/` vytvorime subor `test.php` s obsahom:
```php
    <?php
    	phpinfo();
    ?>
```
 - ulozime a otvorime v prehliadaci, napr.: `www.priklad.xyz/test.php`

#### Ako zapnut v Apache2 modul na kompresiu posielaneho obsahu:
 - aktivujeme modul: `$ sudo a2enmod deflate`
 - dalej mozeme upravit konf. subor `/etc/apache2/mods-enabled/deflate.conf`:
 - medzi tag-y `<IfModule mod_filter.c>` a `</IfModule>` vlozime `DeflateCompressionLevel 7`
   - napr. tato direktiva zvysi uroven kompresie z predvoleneho stupna `6` na `7` 
   - vyssia kompresia prenasa menej dat, ale zvysuje naroky na CPU, rozsah je `1` az `10`

#### Ako zapnut vstavane monitorovanie servera Apache2:
 - aktivujeme modul: `$ sudo a2enmod status`
 - dalej upravime konfiguraciu v subore: `/etc/apache2/mods-available/status.conf`
   - v sekcii medzi `<Location /server-status>` a `</Location>` pridame napr. riadok:
 
    `Require ip 192.168.1.0/24 1.2.3.4 192.0.2.150`
 
   - definujeme, z ktorych IP adries je mozne otvarat: `www.priklad.xyz/server-status`
 - restartujeme proces: `$ sudo systemctl reload apache2`
 - nasledne mozeme v prehliadaci otvorit: `www.priklad.xyz/server-status?refresh=2`
 - na test mozeme pouzit program *Apache Benchmark*, z balika `apache2-utils`
   - pouzijeme prikaz napr.: `$ ab -n 1000 -c 100 http://192.168.1.244/`
   - prikaz vytvori `1000` poziadavok na server, s tym, ze sucasnych dovoli max. `100`
   - dalsie informacie: `$ man ab`

#### Ako zablokovat na Apache2 indexovy vypis suborov, tzv. *file listing*:
- do konf. suboru `vhost` alebo globalnej konfiguracie vlozime:
```apache
    <Directory /var/www/html>
            Options -Indexes

    </Directory>
```

- *POZOR*, ak pouzijeme v konf. `+` alebo `-` vsetky moznosti `Options` *musia* obsahovat `+`/`-`
- nasledne: `$ sudo systemctl reload apache2`

Tip: Ako vypnut *podpis* servera, napr.: `Apache/2.4.41 (Ubuntu) Server at 192.168.1.244 Port 80`
 - upravime subor: `/etc/apache2/conf-available/security.conf` najdeme `ServerSignature On`
 - zmenime na: `ServerSignature Off` potom: `$ sudo systemctl reload-or-restart apache2`
 - je este vhodne zmenit `ServerTokens OS` na `ServerTokens Prod` a restartovat Apache2

### Zaklady prace s automatizacnym nastrojom Ansible:
Ako programom *Ansible* nainstalovat program `nmap` pomocou systemu *APT*:
 - instalujeme balik `ansible`, zadame: `$ sudo apt install ansible`
 - vytvorime si `inventar` zariadeni, napr. vytvorime subor `hosts`, kde napr. vlozime:
```ansible
    [servers]
    vps1 ansible_host=192.168.1.242 ansible_user=ansmin
    vps2 ansible_host=192.168.1.245 ansible_user=ansmin
    vps3 ansible_host=192.168.1.246 ansible_user=ansmin
```

 - ulozime subor s nastaveniami, tento priklad predpoklada *PKI Auth*, prihlasovanie (SSH klucom)
 - spustime: `$ ansible -i hosts servers -m apt -a "name=nmap state=present" --become -K`
   - prikaz vyziada *SUDO* heslo s `--become -K` pre zariadenia zo skupiny `servers`
   - prikaz vyuziva modul `apt` s nastavenim `name=nmap state=present`
   - ked chceme balik odstranit, zmenime nastavenie modulu: `name=nmap state=absent`
   - ked chceme spustit *APT full-upgrade* zmenime nastavenie modulu: `upgrade=full`
   - ked chceme vycistit nepotrebne zavislosti: `autoremove=yes autoclean=yes`

Tip: Ako vypisat dostupne ansible moduly: `$ ansible-doc -l`

Tip: Na privatny SSH kluc mozeme nastavit prava `read-only`, zadame: `$ chmod u-w .ssh/id_rsa`
 - pripadne sa mozu zvazit suborove *ACLka*

### Zaklady prace s balickovacim systemom *Zypper* v systeme OpenSUSE Leap:
 - aktualizacia DB balickov: `$ sudo zypper refresh`
 - instalacia aktualizacii: `$ sudo zypper update`
 - instalacia balicka `nmap`, bez dotazov: `$ sudo zypper install --no-confirm nmap`
 - alebo skratena verzia: `$ sudo zypper -n in nmap`
 - vymazanie balika: `$ sudo zypper remove nmap`
   - opatrne: bez dotazov zmaze balik, doplnime parameter `-n`
 - hladanie balickov v DB: `$ sudo zypper search nmap`
 - vypisanie dostupnych softwarovych *zaplat*: `$ sudo zypper patches`
 - instalacia softwarovych *zaplat*: `$ sudo zypper patch`
 - dalsie informacie v: `$ man zypper`

### Zaklady prace so SAN protokolom iSCSI:

#### Vytvorenie iSCSI targetu *(SAN-server)* na OS Fedora Server 35:

- instalujeme *iSCSI Target* nastroj: `$ sudo dnf -y install targetcli`

- vytvorime tzv. *File-IO* adresar pre disky/LUNy, napr.: `$ sudo mkdir /var/lib/iscsi_pool1/`

- spustime iSCSI nastroj: `$ sudo targetcli`
  - poznamka: v nastroji *TargetCLI* sa daju pouzivat prikazy `cd ..`, `pwd`, `ls` a `relativne cesty`
- dalej pracujeme s Shell interpretom nastroja *TargetCLI*
 
- prepneme sa do rezimu *backstores/fileio*, teda: `/> cd backstores/fileio`

- vytvorime 15GB image: `/backstores/fileio> create disk01 /var/lib/iscsi_pool1/disk01.img 15G`

- prepneme sa do rezimu */iscsi*, teda: `/backstores/fileio> cd /iscsi`

- vytvorime definicu *Target-u*, teda jeho IQN: `/iscsi> create iqn.2022-03.lpic3.suse1:www.target01`

- prepneme sa do rezimu *konkretneho Target-u*, teda: `/iscsi> cd iqn.2022-03.lpic3.suse1:www.target01/`

- prepneme sa do rezimu *TPG - LUNs*, teda: `/iscsi> cd iqn.2022-03.lpic3.suse1:www.target01/tpg1/luns`
  - *TPG* - Target Portal Group, sietova reprezentacia iSCSI Target-u
  - *LUN* - Logical Unit Number, logicka jednotka pre SCSI, particia/disk

- nasledne vytvorime LUN prepojeny s File-IO imagom:

`/iscsi/iqn.20...t01/tpg1/luns> create /backstores/fileio/disk01`

- prepneme sa do rezimu *TPG1*, teda:

`/iscsi/iqn.20...t01/tpg1/luns> cd /iscsi/iqn.2022-03.lpic3.suse1:www.target01/tpg1`

- dalej nastavime autentifikaciu na *CHAP*: `/iscsi/iqn.20...target01/tpg1> set parameter AuthMethod=CHAP`

- prepneme sa do rezimu *ACLs*, teda: `/iscsi/iqn.20...t01/tpg1> cd acls`
  - ACL : Access Control List, pravidla na riadenie pristupu *k LUNom*

- zadefinujeme, ktory *Initiator-IQN (client)* ma prisup na dany LUN:

`/iscsi/iqn.20...t01/tpg1/acls> create iqn.2022-03.lpic3.suse1:www.node01.init01`

- prepneme sa do rezimu *Initiator-IQN*, teda:

`/iscsi/iqn.20...t01/tpg1/acls> cd iqn.2022-03.lpic3.suse1:www.node01.init01/`

- nastavime meno uzivatela: `/iscsi/iqn.20...node01.init01> set auth userid=lpic3iscsi`

- nastavime CHAP heslo pre uzivatela: `/iscsi/iqn.20...node01.init01> set auth password=iscsi.2022`

- celu konfiguraciu overime s: `/iscsi/iqn.20...node01.init01> ls /`

- ukoncime pracu v *TargetCLI*, cim sa ulozi konfiguracia: `/iscsi/iqn.20...node01.init01> exit`
  - konfiguracia je ulozena v subore: `/etc/target/saveconfig.json`

- overime funkcnost iSCSI TCP portu: `$ sudo ss -tanp | grep 3260`

- zabezpecime start sluzby *iSCSI Target* po reboote: `$ sudo systemctl enable target`

- overime stav sluzby `target.service`, teda: `$ sudo systemctl status target`

- zapneme/aktivujeme sluzbu `target.service`, teda: `$ sudo systemctl start target`

- overime stav sluzby `target.service`, teda: `$ sudo systemctl status target`

- povolime TCP portu pre iSCSI na firewalle: `$ sudo firewall-cmd --permanent --add-service=iscsi-target`

- konfiguraciu firewallu overime s: `$ sudo firewall-cmd --list-all`

Poznamka: iSCSI target sa da prevadzkovat v Cluster-y nad systemom DRBD.

Tip: Ako v OS "Fedora Server 35" nainstalovat NetworkManager-TUI: `$ sudo dnf install NetworkManager-tui`

#### Vytvorenie iSCSI initiatora *(SAN-klient)* na OS OpenSUSE Leap 15.3:

- instalacia softwaroveho Initiatora: `$ sudo zypper -n install open-iscsi`
- pracujeme so sluzbami `iscsi` a `iscsid`
- dolezite konfiguracne subory: `/etc/iscsi/iscsid.conf` a `/etc/iscsi/initiatorname.iscsi`
- initiator moze byt HW (napr. sietova karta s TCP/iSCSI offloadingom) alebo softwarovy

- pridame Initiatora do zoznamu, podla vytvoreneho ACL IQN: `$ sudo vim /etc/iscsi/initiatorname.iscsi`
- pridame riadok napr.: `InitiatorName=iqn.2022-03.lpic3.suse1:www.node01.init01`

- nasledne upravime konfiguraciu suboru: `/etc/iscsi/iscsid.conf`
- odkomentujeme: `node.session.auth.authmethod = CHAP`
- odkomentujeme a pridame meno/heslo:
```
node.session.auth.username = MOJE_MENO
node.session.auth.password = MOJE_HESLO
```
Nasledne restartujeme iSCSI sluzby: `$ sudo systemctl restart iscsi iscsid`

Spustime *discovery* voci Target device: `$ sudo iscsiadm -m discovery -t sendtargets -p 192.168.2.X`
 - v pozadi sa vytvoria adresare: `/etc/iscsi/nodes/` a `/etc/iscsi/send_targets/`
 - mozeme overit status, napr. prikazom: `$ sudo iscsiadm -m node -o show`

Nasledne prihlasime/pripojime initiatora LUN/disku prikazom: `$ sudo iscsiadm -m node --login`
 - overime prikazom `$ sudo iscsiadm -m session -o show`

Pripojenie disku overime prikazmi napr. `$ cat /proc/partitions` alebo `$ lsblk`
 - najdeme spravy o pripojeni noveho disku (napr. `/dev/sdb`) aj v Syslogu: `$ sudo journalctl -f`

Nasledne vytvorime particiu, napr. pomocou nastrojov `fdisk`, `cfdisk`, `parted`, a pod.
 - potom novu particiu naformatujeme suborovym systemom podla poziadavky: `$ sudo mkfs.XYZ /dev/sdX`

Ak chceme automaticke pripajanie disku po reboote:
- v subore `/etc/iscsi/iscsid.conf` odkomentujeme riadok: `node.startup = automatic`

Na vytvorenie *mount-pointu* po reboote si zistime `UUID` particie napr. s: `$ sudo blkid`
 - nasledne do suboru `/etc/fstab` pridame riadok, napr.:
```
UUID=aa03eabf-10a9-41d9-a1eb-149682d0c44f /mnt/san1d1 btrfs _netdev,x-systemd.automount 0 0
```

Po reboote systemu mozeme overit napr. s: `$ sudo mount | grep san1` alebo prikazom: `$ sudo lsblk`
 - alebo napr. s: `$ sudo ls -l /dev/disk/by-path/`

Poznamka: ak je potrebne, je mozne *discovered* targety vymazat, alebo docasne odhlasit:
 - vymazeme: `$ sudo iscsiadm -m node -T iqn.2022-03.lpic3.suse1:www.target01 -o delete`
 - odhlasime: `$ sudo iscsiadm -m node -T iqn.2022-03.lpic3.suse1:www.target01 -u`
   - po ukonceni cinnosti sa da znova pripojit restartom sluzieb `iscsi` a `iscsid`

Poznamka: v systeme OpenSUSE Leap sa da pouzit na konf. iSCSI Initatora TUI nastroj: `$ sudo yast2`
 - *TUI* - Terminal User Interface
 - instalujeme: `$ sudo zypper -n in yast2-iscsi-client`
 - v menu volime `Network Services` -> `iSCSI Initiator` -> `sipkou doprava` na `Connected Targets`
   - v tomto submenu sa uz mozeme klavesom `Tab` prepnut na moznosti `Add` / `Edit` / `Disconnect`

* * *
Zaklady prace s HA - High Availability Cultermi v systeme GNU/Linux
-----------------
Hlavne stavebne kamene HA Cluster-ov na systeme GNU/Linux: `Pacemaker` a `Corosync`.

Na pracu s HA-lusterom je vhodne mat *DNS zaznami typu A/PTR uzlov*, pripadne zaznami v `/etc/hosts`

#### Trocha teorie: CIB - Cluster Information Base, Stav Clustra v pamati systemu
 - ako kopia existuje na kazdom uzle, subor sa *NESMIE* rucne upravovat
 - na spravu CIB sa pouziva nastroj `cibadmin`, napr. vypis databazy: `$ sudo cibadmin -Q | less`
 - proces *Cluster Resource Management Daemon* `crmd`, umoznuje pristup k tejto databaze
   - zabezpecuje dalej riadiacu komunikaciu medzi uzlami cluster-a
 - dalsi komponent *Local Resource Management Daemon*, teda `lrmd` zabezpecuje spravu lokalnych zdrojov
 - dalsi komponent na spravu politik v Clustery, *Policy Engine* `pengine`
 - dalsi komponent *Transition Engine* `tengine`
 - dalsi komponent `stonithd` zabezpecuje vybavovanie *STONITH* poziadavok
   - *STONITH* - Shoot The Other Node in The Head, pripadne tzv. *Node Fencing*
 - v RedHat based distribuciach sa pouziva nastroj `pcsd`, ako rozhranie ku `Corosync` a `Pacemaker`
   - pouziva sa prikazy: `$ sudo pcs ...`
 - alternativne sa pouziva nastroj CRM Shell `crmsh`, ktory ma prikazy: `$ sudo crm ...`

#### Priklad instalacie Multicast clustra na systeme OpenSUSE Leap s nastrojom `crm`:
 - na uzloch instalujeme: `$ sudo zypper in ha-cluster-bootstrap`
 - nasladne na *hlavnom* uzle spustime: `$ sudo crm cluster init`
 - na dalsich clenoch spustime `join` na *hlavny* uzol: `$ sudo crm join -c <hostname>`
   - treba sa pripravit na manazment PKI klucov v SSH pre uzivatelov `root` a `hacluster`
   - z tohto vyplvyva aj relevantne zabezpecenie/izolacia sietoveho segmentu
 - instalaciu overime s `$ sudo crm_mon` alebo: `$ sudo crm status`
   - dalej mozeme pouzit: `$ sudo systemctl status corosync`
 - konfiguraciu mozeme overit s: `$ sudo crm configure show`

#### Dalsia praca s nastrojom `crm`:
 - interpret podporuje tzv. *TAB completion*, ked nevieme presne prikaz
 - alebo sa da spustit v interaktivnom rezime s: `$ sudo crm`
 - vypisanie konfiguracie cluster-a: `$ sudo crm configure show`
   - mozeme vidiet ze pridelene zdroje v clustery sa definuje ako tzv. `primitive`
 - ak chceme upravit konfiguraciu clustera, pouzijeme: `$ sudo configure edit`
 - dalsie zdroje pridelime v interaktivnom shelly: `$ sudo crm configure`
 - napr. v interaktivnom rezime pridame dalsiu *Virtual IP*, pouzijeme prikaz:
```
crm(live)configure# primitive newIP ocf:heartbeat:IPaddr2 params ip=192.168.255.30 cidr_netmask=24
```

 - ak chceme po prikaze nieco upravit, pouzijeme prikaz `edit`, teda: `crm(live)configure# edit`

#### Praca s RA - Resource Agents:
 - tito agenti spravuju zdroje, napr.: *OCF* - Open Cluster Framework
 - vypiseme triedy agentov pre zdroje: `$ sudo crm ra classes`
 - presnejsi vypis RA z triedy OCF: `$ sudo crm ra list ocf`
 - OCF ma *svoje* skripty, ako napr. *SystemD*
 - informacie o konkretnom RA ziskame s: `$ sudo crm ra info apache`

Tip: Ako ulozit nastrojom `crm` konfiguraciu clustera do suboru s datumom v nazve:
 - napr. prikaz: `$ sudo crm configure save zaloha-clus-$(date +%d-%m-%Y).txt`
 - *POZOR* na testovanie v LAB prostredi mozeme zmazat CIB: `$ sudo cibadmin -E --force`
 - nasledne mozeme konfiguraciu obnovit: `$ sudo crm configure load push zaloha-clus-12-03-2022.txt`

#### Priklad instalacie Unicast clustra v systeme CentOS Stream 9 - nastroj `pcs`:
 - pridame repozitar: `$ sudo dnf install epel-release`
 - aktivujeme v `/etc/yum.repos.d/centos-addons.repo` repo. `highavailability` uprava na `enabled=1`
 - aktualizujeme repo.: `$ sudo dnf update`
 - instalacia: `$ sudo dnf --enablerepo=highavailability -y install pacemaker corosync pcs`
 - nastavime, aby sluzby startovali po reboote: `$ sudo systemctl enable pacemaker corosync pcsd`
 - overime s: `$ sudo systemctl status pacemaker corosync pcsd | grep loaded`
 - upravime konf. firewall-u: `$ sudo firewall-cmd --permanent --add-service=high-availability`
 - restartujem firewall proces: `$ sudo firewall-cmd --reload`
 - nastavime heslo pre specialneho uzivatela: `$ sudo passwd hacluster`
 - pokracujeme Autentifikaciou uzlov: `$ sudo pcs host auth cent1 cent2 cent3`
   - pre diagnostiku mozeme na koniec prikazu pridat: `--debug` 
 - diagnostika: `$ sudo pcs status pcsd cent1 cent2 cent3`
   - detailensjie diagnostika: `$ sudo pcs status --full`
 - dalej zostavime cluster: `$ sudo pcs cluster setup centos-clus1 cent1 cent2 cent3 --start --enable`
 - overime s: `$ sudo pcs status`
 - stav vsetkych potrebnych sluzieb overime s: `$ sudo systemctl status pacemaker corosync pcsd`

#### Dalsia praca s Cluster nastrojom `pcs`:
 - tiez podporuje *TAB completion*, s niekolkymi vynimkami
 - je potrebne nainstalovat balicek: `$ sudo dnf in bash-completion`
 - najskor overime ci bezi proces `pcsd`, prikaz: `$ sudo systemctl status pcsd`
 - ako rucne upravit CIB konfiguraciu s `pcs`, prikaz: `$ sudo pcs cluster edit`
   - ak nemame definovanu premennu `$EDITOR`, tak: `$ sudo export EDITOR=$(which vim)`
   - dalsie editory: `emacs`, `nano`, `pico`, `joe`, `mcedit`, ...
 - ako vypisat dostupne zdroje clustera: `$ sudo pcs resource list | less`
 - ako vypisat popis urciteho zdroja `IPaddr2` pre cluster: `$ sudo pcs resource describe IPaddr2`
 - ako vytvorit zdroj *Virtualna HA IP adresa* nastrojom `pcs`:
   - prikaz: `$ sudo pcs resource create mojaIP IPaddr2 ip=192.168.255.30 cidr_netmask=24`
   - overime s: `$ sudo pcs resource status mojaIP`
   - minimalne v danom L2 segmente by malo odpovedat aj: `$ ping -c2 192.168.255.30`

Mozeme menit aj tzv. genericke vlastnosti Cluster-a, ktore sa priamo netykaju zdrojov (resources):
 - vypisanie vlastnosti: `$ sudo pcs property config --all | less`
 - napr. mozeme vlastnost `stonith-enabled` upravit: `$ sudo pcs property set stonith-enabled=true`

Podobne pracuje s vlastnostami/properties aj nastroj `crm`: `$ sudo crm configure get_property`
 - podobne upravime vlastnost s: `$ sudo crm configure property stonith-enabled=no`
 
#### Zjednoduseny priklad ako vytvorit WebServer cluster pomocou `crm` na OS OpenSUSE Leap 15.3:
 - je potrebne nainstalovat samotny WebServer Apache2: `$ sudo zypper -n install apache2`
 - otvorime konfiguraciu zdrojov cluster-a prikazom: `$ sudo crm configure edit`
 - pridame dve definicie zdrojov, konkretne Virtualnu IP a samotny proces WebServera Apache2:
```
primitive ip-apache ocf:heartbeat:IPaddr2 \
        params cidr_netmask=24 ip=192.168.255.20 \
        op monitor interval=1 timeout=4
primitive service-apache ocf:heartbeat:apache \
        op stop interval=0 timeout=60 \
        op start interval=0 timeout=60 \
        op monitor interval=10 timeout=30
```

 - po ulozeni a zavreti editora sa zmeny aplikuju na *cely Cluster*
 - stav clustera overime s: `$ sudo crm_mon`
 - pripadne aktualizujeme stav a pridelenie zdrojov: `$ sudo crm resource cleanup`
 - nasledne je potrebne na *vsetkych* uzloch povolit HTTP port na firewalle:
```bash
    $ sudo firewall-cmd --permanent --add-service=http
    $ sudo firewall-cmd --reload
```

Poznamka: zdroj je kvoli zjednoduseniu dostupny len na realnej IP adrese uzla, na ktorom bezi `service-apache`
 - zistime s: `$ sudo crm_mon`

#### Zjednoduseny priklad ako vytvorit WebServer cluster pomocou `pcs` na CentOS Stream 9:
 - je potrebne nainstalovat samotny WebServer Apache2: `$ sudo dnf -y in httpd`
 - *POZOR*, na TEST je potrebne vypnut STONITH/Fencing: `$ sudo pcs property set stonith-enabled=false`
 - vytvorine vIP: `$ sudo pcs resource create apache-ip IPaddr2 ip=192.168.255.29 cidr_netmask=24`
 - overime s: `$ sudo pcs resource status`
 - nasledne vytvorime Apache2 zdroj clustera: `$ sudo pcs resource create apache-service apache`
 - overime s: `$ sudo pcs resource status`
 - otvorime konfiguraciu zdrojov cluster-a prikazom: `$ sudo crm configure edit`
 - nasledne je potrebne na *vsetkych* uzloch povolit HTTP port na firewalle:
```bash
    $ sudo firewall-cmd --permanent --add-service=http
    $ sudo firewall-cmd --reload
```
Poznamka: web je kvoli zjednoduseniu dostupny len na real. IP uzla na ktorom bezi `service-apache`
 - zistime s: `$ sudo pcs resource status`
 
Tip: Ako vypisat stav technologie *Quorum*, ktora zabranuje vzniku *split-brain* scenarov:
 - prilaz: `$ sudo corosync-quorumtool`
 - obvzvlast nebezpecny je efekt *split-brain* pre uloziska, teda *storage resources*
 - ciastocne sa da stav kvora sledovat prikazom: `$ sudo crm_mon`

#### Pri zostavovani clustra nastrojom `pcs`:
 - teda prikazom: `$ sudo pcs cluster setup`, mame moznosti:
 - parameter `--wait_for_all` - vypocet kvora sa zacne az po zacleneni vsetkych uzlov/nodes
 - parameter `--auto_tie_breaker` - pri 50% "hlasov" sa vitaz urci ako uzol s najnizsim ID
 - parameter `--last_man_standing` - kvorum sa prepocitava kazdych 10s
   - treba skombinovat s `--wait_for_all` a nasledne umoznuje postupne *vypinanie* uzlov z clustra 
 - parameter `--two_node` umoznuje "bezat" cluster z 2 uzlov

#### V distribucii OpenSUSE je konfiguracia Cluster kvora:
 - dostupna v subore `/etc/corosync/corosync.conf`
 - priklad na konfiguraciu kvora v subore `corosync.conf`:
 - zmeny samozrejme robime v LABe, inak treba robit *off-peak udrzbu* a mat pripravene zalohy konf.
```
quorum {
        provider: corosync_votequorum
        last_man_standing: 1
        wait_for_all: 1
        auto_tie_breaker: 1
        auto_tie_breaker_node: lowest
        two_node: 1
}
```

- po ulozeni nasledne restartujeme proces: `$ sudo systemctl restart corosync`
- nove parametre overime s: `$ sudo corosync-quorumtool`

Poznamka: ak by sme robili upravy v `corosync.conf` na OS s `pcs`, mozeme zmeny distribuovat na ostatne uzly:
  - pouzijeme prikaz: `$ sudo pcs cluster sync`
  - nasledne je potrebne znova spustit cluster: `$ sudo pcs cluster reload corosync`

#### Zaklady konceptu Node Fencing/STONITH:
 - problematicky uzol treba *odrezat* z Clustera, fencing ma viacero druhov
 - druh *Power fencing*: ked mame pristup ku kontrolerom napajania, odrezeme napajenia uzla (UPS/PDU)
 - druh *Fabric fencing*: uzol odrezeme od storage konektivity, teda od iSCSI, resp. FibreChannel-u
 - samozrejme su k dispozicii dalsie moznosti Fencingu
 - k dispozicii su *Fencing agenti*, teda: `disk`, `hypervisor`, `power switch`, `management board`, `test agent`
   - agent `disk` - zmedzi uzlu pristup na disk(y)
   - agent `hypervisor` - vypne VM uzol, v prostredi GNU/Liunux sa napr. pouziva projekt `libvirt`
   - agent `power switch` - vypne napajanie, cez API kontrolera napajania na PDU/UPS
   - agent `management board` - vypne fyz. server cez Out-Of-Band Mng. (iLO, iDRAC, IBM-RSA, IPMI) 
   - agent `test agent` - sluzi na testovanie fencingu, v praxi nedoporucovane
 - napr. v Systeme CentOS si mozeme nainstalovat agenta `fence-agents-apc`: 
   - prikaz: `$ sudo dnf -y in fence-agents-apc`
   - dalsie informacie o agentovi ziskame napr. z: `$ man fence_apc`
 - dalsi agent `fence-agents-ipmilan` je uzitocny, pretoze vykovana Fencing cez standard *IPMI*
 - na *CentOS* mozeme ziskat informacie o *STONITH/Fencing* agentoch pre Pacemaker: `$ pcs stonith list`
   - dalsie info. o konkretnom agentovi ziskame napr. s: `$ sudo pcs stonith describe fence_ipmilan`
 - na *OpenSUSE* vypiseme agentov: `$ sudo stonith -L`
   - presnejsie informacie o agentoch ziskame s: `$ sudo stonith -h | less`

#### Konfiguracia Fencing-u v systeme CentOS Stream 9:
 - da sa pouzit *Hypervisor* Fencing "device"/agent, instalujeme: `$ sudo dnf -y in fence-virtd`
   - tento agent sa pouziva pri hypervizore *KVM*, kazdy hypervizor musi mat `fence-virtd`
   - hypervizory musia byt na spolocnom Multicast segmente a musia zdielat spolocny *PSK kluc*
 - *POZOR*, na TEST mozeme "odstavit" VM instanciu prikazom: `$ sudo echo c > /proc/sysrq-trigger`
 - akciu *STONITH* mozeme rucne vykonat aj prikazom: `# sudo pcs stonith <hotname>`

#### Ako pouzivat SBD Fencing na VM:
 - je potrebne do kernelu nacitat modul `softdog`
 - *SBD* - STONITH Based on Disk
 - na rozdiel od fyz. HW, na VM chyba SCSI *Watchdog*, preto treba nacitat software verziu:
 - overime loading kernel modulov pomocou SystemD: `$ sudo systemctl status systemd-modules-load`
 - na nacitanie modulu `softdog`, vytvorime v `/etc/modules-load.d` subor `watchdog.conf`
 - nasledne do tohto suboru vlozime riadok s nazvom kernel modulu, teda: `softdog`
 - dalej restartujeme proces: `$ sudo systemctl restart systemd-modules-load`
 - pritomnost modulu v kerneli overime s: `$ sudo lsmod | grep soft`

#### Praca s *Cluster Resources*, teda zdroje, ktore dokaze cluster poskytovat:
 - mame k dispozicii tieto typy zdrojov: `Primitive`, `Clone`, `Multi State (Master/Slave)`, `Group`
   - typ `Primitive` - singularny zdroj spravovany resource manazerom clustra, ma "bezat" iba raz
   - typ `Clone` - zdroj, ktori spravuje cluster a bezi na viacerych uzloch viac-krat, napr. cLVM
   - typ `Multi State (Master/Slave)` - zdroje bezia v hierarchii, priklad je *DRBD*
   - typ `Group` - skupina zdrojov, teda skupina `Primitives` a `Clones`, napr. *HA Webserver*
     - umoznuje definovat *obmedzenia zdrojov/Resource constraints*, ktore poskytuje cluster
 - pojem *Resource Stickiness* definuje, *kde sa ma rozbehnut* zdroj po obnove z fail situacie
 - ako hladat urcity *Resource script* na disku, napr. *IPaddr2*, prikaz: `$ sudo find / -name IPaddr2`
 - nastrojom `crm` mozeme otvorit interaktivny *Cluster Management* shell: `$ sudo crm`
   - definovane zdroje vypiseme s `crm(live/suse1)# resource status` alebo s: `$ sudo crm_mon`
 
#### Praca s obmedzeniami zdrojov *Resource constraints*:
 - rozdelujeme na tri typy: `Location`, `Colocation` a `Order`:
   - typ `Location` - na ktorom uzle ma *bezat* dany zdroj/resource, preferencia uzla
   - typ `Colocation` - s ktorym dalsim zdrojom, ma/nema bezat dany zdroj
   - typ `Order` - pred ktorym alebo za ktorym zdrojom ma dany zdroj *bezat*
 - prikazy `$ sudo crm migrate` a `$ sudo crm resource move`, prikazu obmedzenia danemu zdroju
   - prikazmi `$ sudo crm unmigrate` resp. `$ sudo crm resource clear` tieto obmedzenia odstranime
 - pomocou nastroja `crm` mozeme vypisat stav riadenia obmedzeni: `$ sudo crm_simulate -sL`
 - doporuceny dizaj je vsak pouzivat koncept *Resource Groups*

#### Praca s cluster obmedzeniami pomocou konceptu *Resource Groups*:
 - doporucuje sa vytvarat obmedzenia na skupiny/groups pre jednoduchsiu spravu zdrojov
 - napr. vytvorime dva `IPaddr2` zdroje, ktore zaradime do skupiny `IPgroup`:
   - prikaz: `$ sudo pcs resource create ip1 IPaddr2 ip=10.0.0.1 cidr_netmask=24 --group IPgroup`
   - prikaz: `$ sudo pcs resource create ip2 IPaddr2 ip=10.0.0.2 cidr_netmask=24 --group IPgroup`
   - vzniknutu skupinu zdrojov overime prikazom: `$ sudo pcs status`

 - postup zaradovania zdrojov do skupiny pomocou nastroja `crm`:
 - otvorime konfiguraciu clustera s: `$ sudo crm configure edit`
 - pridame riadok, ktory dva (existujuce) IP zdroje `admin-ip` a `dalsiaIP` zaradi do group `IPgroup`

    group IPgroup admin-ip dalsiaIP

 - subor ulozime a overime, napr. prikazom: `$ sudo crm_mon`

Poznamka: ako na *troubleshooting*, teda hladanie a riesenie problemov s *Resource Groups*:
 - nastrojom `pcs` overime stav clustra: `$ sudo pcs status`
 - dalej mozeme skontrolovat log `/var/log/messages` alebo s `$ sudo journalctl`
   - v programe `journalctl` sa klavesovou skratkou `Shift + g` resp. `G` prepnema na koniec logu

#### Praca s konceptom *Cluster Resource Clones*:
 - umoznuje bezat primitivy alebo skupiny na viacerych uzloch:
 - pocet klonov byva zvycajne rovnaky ako pocet uzlov, ale moze sa obmedzit pocet klonov
 - typicky sa pouziva nastavenie `interleave=true`, ktore umoznuje bezat ostatne klony nezavisle
   - napr. ked sa jeden z klonov zruti

#### Priklad ako vytvorit Cluster s *FTP server zdrojom* pomocou `pcs`:
 - najskor *na vsetkych* uzloch instalujeme FTP server: `$ sudo dnf -y in vsftpd`
 - aktivujeme na uzloch FTP server: `$ sudo systemctl enable vsftpd && sudo systemctl start vsftpd`
 - potom pomocou nastroja `pcs` vytvorime 2 zdroje a zaradime ich to skupiny `ftp-service`:
 - prikaz: `$ sudo pcs resource create ftp-ip IPaddr2 ip=10.0.0.123 cidr_netmask=24 --group ftp-group`
 - prikaz: `$ sudo pcs resource create ftp-service systemd:vsftpd --group ftp-group`
 - overime prikazom: `$ sudo pcs status`
 - nasledne obmedzime, tak aby skupiny `apache-group` a `ftp-group` nebezali na rovnakom uzle:
   - prikaz: `$ sudo pcs constraint colocation add apache-group with ftp-group -10000`
 - upravime poradie startovania zdrojov: `$ sudo pcs constraint order apache-group then ftp-group`

#### Priklad tvorby zdrojov clustera s obmedzeniami/constraints pomocou nastroja `crm`:
 - upravujeme konfiguraciu clustera pomocou: `$ sudo crm configure edit`
 - ako priklad vytvorime podobne cluster *FTP server* v resource skupine `ftp-group`:
   - na uzloch instalujeme: `$ sudo zypper -n in vsftpd`
   - na uzloch aktivujeme server: `$ sudo systemctl enable vsftpd && sudo systemctl start vsftpd`
   - nasledne definujeme zdroje do skupiny `ftp-group`, upravime konf.: `$ sudo crm configure edit`:
```
primitive ftp-ip IPaddr2 \
        params nic=eth0 cidr_netmask=24 ip=192.168.255.200 \
        op monitor interval=10 timeout=40
primitive ftp-service systemd:vsftpd
group ftp-group ftp-ip ftp-service
```
   - aplikujeme zmeny a overime napr. s: `$ sudo crm status`
 - dalej pridame do konfiguracie podobne obmedzenia/constraints: `$ sudo crm configure edit`
```
order ftp-after-apache apache-group ftp-group
colocation web-not-ftp -10000: ftp-group apache-group
```
   - aplikujeme zmeny a overime napr. s: `$ sudo crm status`
 - na testovanie je potrebne povolit FTP sluzbu na firewalle:
   - prikazy: `$ sudo firewall-cmd --permanent --add-service=ftp && sudo firewall-cmd --reload`
 - nasledne mozeme dostupnost FTP sluzby overit napr. prikazom: `$ nc 192.168.X.Y 21`
   - dalsie informacie o nastroji `netcat` napr. v: `$ man nc`

#### Zaklady manazmentu zdrojov Clustera s nastrojmi `pcs` a `crm`:
 - prikaz: `$ sudo pcs resource enable` zapne zdroj
 - prikaz: `$ sudo pcs resource disable` vypne zdroj
 - prikazmi restartujeme zdroje: `$ sudo pcs resource restart` a `$ sudo crm resource restart`
 - prikazmi upravujeme zdroje: `$ sudo pcs resource update` resp.: `$ sudo crm configure edit`
 - na ladenie pouzijeme: `$ sudo pcs resource debug-start <resource>`
 - na restart resetujeme tzv. *Failcount*: `$ sudo pcs resource refresh`
 - na udrzbu mozeme vypnut/zapnut manazment zdroja cluster stackom:
   - prikazy: `$ sudo pcs resource [un]manage` resp.: `$ sudo crm resource [un]manage`
 - ako presuvat zdroje na ine uzly: `$ sudo pcs resource relocate`
 - ako definovat limity zdrojov, priklad: `$ sudo pcs resource utilization <resource> ram=20 cpu=10`
   - pre nastroj `crm`: `$ sudo crm resource utilization <resource> ram=20 cpu=10`
     - treba mi pozriet presnejsie
 - na udrzbu, mozeme vypnut cluster sluzby na uzle: `$ sudo pcs cluster stop <adresa-nodeX>`
 - po upravach/udrzbe, znova spustime: `$ sudo pcs cluster stop <adresa-nodeX>`
 - stav overime s: `$ sudo pcs status`
 - zapneme/vypneme prihlasovanie do clustera: `$ sudo pcs cluster {disable|enable} <adresa-nodeX>`
 - pridavanie/odstranovanie uzlov: `$ sudo pcs cluster node {add|remove} <adresa-nodeX>`
   - nasledne je potrebne autentifikovat novy uzol: `$ sudo pcs host auth <adresa-nodeX>`
   - overime s: `$ sudo pcs status`
 - na odstranenie uzla pouzijeme uvedene: `$ sudo pcs cluster node remove <adresa-nodeX>`
   - dalej je potrebne odstranit STONITH proces: `$ sudo pcs stonith delete <adresa-nodeX>`
 - ked potrebujeme docasne vyradit uzol: `$ sudo pcs node [un]standby <adresa-nodeX>`
   - rozdiel oproti vypnutiu, je ucast na Qourum procese
   - overime s: `$ sudo pcs status` alebo s: `$ sudo pcs status nodes`

#### Dalsie tipy a triky pre nastroje `crm` a `pcs` na spravu uzlov a zdrojov v Clustroch:
 - prikaz: `$ sudo crm cluster add`
 - nastroj `crm` na uvedenie uzla do modu `standby`: `$ sudo crm node standby <nazov-uzla>`
   - po upravach *zapneme*: `$ sudo crm node online <nazov-uzla>`
   - nazov uzla ziskame napr z: `$ sudo crm status`

Tip: Ako dat uzol do tzv. *Maintenance Mode*:
 - mod umoznuje udrzbu cluster software ale nema dosah na zdroje
 - prikaz nastavi *Maintenance* mod: `$ sudo crm node maintenance <nazov-uzla>`
 - nasledne po upravach: `$ sudo crm node ready <nazov-uzla>`
 - overime s: `$ sudo crm status`

Tip: Ako na presuvanie zdrojov Clustra na definovane uzly:
 - prikaz presunie resource group na iny uzol: `$ sudo crm resource move apache-group <nazov-uzla>`
 - ak chceme predoslemu uzlu vratit moznost bezat zdroj, tak: `$ sudo crm resource clear apache-group`
   - *POZOR*, spravanie tohto prikazu meni koncept *Resource Stickiness*
 - overime s: `$ sudo crm status`

Tip: Ako na reset Failcount-erov: `$ sudo pcs resource cleanup` resp.: `$ sudo crm resource cleanup`

Tip: Ako vypisat/vlozit skrateny datum: `$ date +%H%h%Y` resp. v skripte: `$(date +%H%h%Y)`

#### Praca s Cluter logmi projektov *Corosync* a *Pacemaker*:
 - loguje sa na 2 urovniach: *Corosync* a *Pacemaker*
 - logy z Corosync-u mozeme sledovat v: `$ sudo tail -f /var/log/cluster/corosync.log`
 - logovanie sa zapina v `/etc/corosync/corosync.conf`, direktiva `to_logfile: yes`
 - logovanie do `std::err`, ktore zachytava Systemd, teda `journalctl` zapneme s `to_stderr: yes`
 - zmenu mozeme replikovat s: `$ sudo pcs cluster sync`
 - nasledne restartujeme *Corosync* s: `$ sudo pcs cluster reload corosync`
 - je vhodne zvazit strategiu a nastroje `logrotate`
 - logy nastroja *Pacemaker* najdeme v `/var/log/pacemaker/pacemaker.log`
 - mozeme pouzit spolocne logy Systemd: `$ sudo journalctl -lu pacemaker.service -u corosync.service`
   - pripadne ich sledovat: `$ sudo journalctl -fu pacemaker.service -u corosync.service`

#### Dalsie priklady na manazment Clustra s nastrojom `pcs`:
 - vytvori zdroj: `$ sudo pcs resource create myDummy ocf:heartbeat:Dummy op monitor interval=60s`
 - aplikujeme obmedzenie na zdroj: `$ sudo pcs constraint location myDummy prefers <adresa-nodeX>`
 - overime s: `$ sudo pcs status`
 - vypiseme obmedzenia: `$ sudo pcs constraint list` alebo s `$ sudo pcs constraint config`
 - ked chceme hladat napr. `location` obmedzenie, hladame toto slovo v: `$ sudo cibadmin -Q | less`
 - dalej dane obmedzenie odstranime: `$ sudo pcs constraint remove location-myDummy-cent2-INFINITY`
 - presunieme zdroj na iny uzol: `$ sudo pcs resource move myDummy`
 - overime s: `$ sudo pcs status` alebo s: `$ sudo pcs resource status`
 - prikazom *odstavime* uzol: `$ sudo pcs node standby <adresa-nodeX>`
 - nasledne *zapneme* uzol: `$ sudo pcs node unstandby <adresa-nodeX>`
 - prikazom vypneme manazment zdroja, umozni zmeny na uzle: `$ sudo pcs resource unmanage myDummy`
 - overime s: `$ sudo pcs resource status`
 - dalej znova aktivujeme manazment zdroja: `$ sudo pcs resource manage myDummy`
 - po teste zmazeme: `$ sudo pcs resource disable myDummy` a `$ sudo pcs resource remove myDummy`

#### Dalsie priklady na manazment Clustra s nastrojom `crm`:
 - editujeme konf. a pridame zdroj `myDummy` a obmedzenie `myDummy-location`:
 - prikaz: `$ sudo crm configure edit` a nasledne vlozime:
```
primitive myDummy ocf:pacemaker:Dummy \
        op monitor interval=60
location myDummy-location myDummy 10000: lpic3-suse1
```
- overime s: `$ sudo crm status` resp. s: `$ sudo crm configure show`
- presunieme zdroj na iny uzol `lpic3-suse2`, zadame: `$ sudo crm resource move myDummy lpic3-suse2`
- tuto migraciu mozeme zmazat v configu alebo s: `$ sudo crm resource clear myDummy`
- prikaz prepne uzol `lpic3-suse1` do `standby` modu: `$ sudo crm node standby lpic3-suse1`
- prikaz prepne uzol `lpic3-suse1` do `online` modu: `$ sudo crm node online lpic3-suse1`
- vypneme manazment zdroja `myDummy`, umozni zmeny na uzle: `$ sudo crm resource unmanage myDummy`
- znova aktivujeme manazment zdroja `myDummy` s: `$ sudo crm resource manage myDummy`
- prepneme uzol do stavu `maintenance`, teda udrzby: `$ sudo crm node maintenance lpic3-suse1`
- vratime uzol do stavu `ready`, teda pripraveny na cinnost: `$ sudo crm node ready lpic3-suse1`
- vsetky zmeny overime s: `$ sudo crm status` resp.: `$ sudo crm configure show`
 
Zaklady prace so *Storage* rieseniami v Cluster prostredi GNU/Linux
----------------

### Ako na instalaciu/nasadenie technologie *iSCSI Multipath*:
 - vyuziva sa fakt, ze *SAN iSCSI Target ma viac sietovych pripojeni*, na ktore sa Initiator pripaja
   - zariadenie v role *iSCSI Initiatora* ma tiez k dispozicii *dalsiu nezavislu SAN konektivitu*
 - technologia umoznuje viacero zaloznych ciest na storage zariadenia (SAN)
 - zalozne cesty su *plne redundantne*, teda nezavisle voci inym cestam (karty, routre, switche...)
 - vacsina distribucii vyuziva tzv. *Device Mapper* implementaciu `dm-multipath`
 - sluzba je prevadzkovana `multipathd` ako daemon/proces
 - na manazment sa vyuziva program: `$ sudo multipath`
 - konfiguracia sa nachadza v subore: `/etc/multipath.conf`
 - zariadenia dostupne cez `dm-multipath` sa nachadzaju v `/dev/mapper`

#### Priklad instalacie riesenia *Device Mapper Multipath* v OS CentOS Stream 9:
 - instalujeme *Device Mapper* (zvycajne byva uz nainstalovany): `$ sudo dnf -y in device-mapper-multipath`
 - zapneme start procesu `multipathd` po reboote, teda: `$ sudo mpathconf --enable --with_multipathd y`
   - prikaz zaroven vygeneruje konfig. subor: `/etc/multipath.conf`
   - dalsie informacie v `$ man mpathconf` a v `$ man multipath.conf`
   - stav sluzby overime s: `$ sudo systemctl status multipathd.service`
 - po viac-nasobnom pripojeni na iSCSI Target, nam *system prideli rozne zariadenia na jeden LUN*
   - toto sa snazi *Multipathing* riesit tym, ze *spoji viacere cesty do jedneho zariadenia*
 - stav dostupnych multipath zariadeni overime s: `$ sudo multipath -ll`
 - tieto zariadenia su dostupne ako `/dev/mapper/mpathX`, `/dev/mapper/mpathX` a pod.

Poznamka: alternativy k systemu CentOS: `CentOS Stream`, `Alma Linux`, `Rocky Linux`, `Oracle Linux`

#### Ako zabezpecit, aby sa system Ubuntu 20.04 neplnil log spravami `multipathd`:
	
    Apr 26 16:10:29 ubuntu2004 multipathd[728]: sda: add missing path
    Apr 26 16:10:29 ubuntu2004 multipathd[728]: sda: failed to get udev uid: Invalid argument
    Apr 26 16:10:29 ubuntu2004 multipathd[728]: sda: failed to get sysfs uid: Invalid argument
    Apr 26 16:10:29 ubuntu2004 multipathd[728]: sda: failed to get sgio uid: No such file or directory

Upravime obsah suboru `/etc/multipath.conf` nasledovne:

Vlozime riadky: 

    defaults {
        user_friendly_names yes
    }
    blacklist {
        devnode "^(ram|raw|loop|fd|md|dm-|sr|scd|st|sda)[0-9]*"
    }

Po ulozeni treba restartovat proces `multipathd` s: `$ sudo systemctl restart multipathd.service`
 
- dodatocne mozeme skontrolovat stav procesu: `$ systemctl status multipathd.service`

### Praca s Cluster Storage riesenim *DRBD - Distributed Replicated Block Device*:
 - riesenie v podstate realizuje *RAID1* ale cez sietove prepojenia
 - zvycajne sa pouzivaju *2 storage uzly*, ktore si navzajom synchronizuju data
 - zakladny *M/S* model vyuziva standardne FS, napr. Ext4, XFS, ...
 - rezim *Multi-master* umoznuje obom stroage uzlom read/write pristup, dvojcestna synchronizacia
 - specialny *Cluster filesystem* je nevyhnutny, napr. GlusterFS, OCFS2, GFS2
 - system DRBD pracuje s replikacnymi modmi:
   - `Protocol A`: Asynchronne zapisovanie, vhodne na "long-distance" replikaciu, znizena spolahlivost
   - `Protocol B`: Semi-synchronne zapisovanie
   - `Protocol C`: Synchronne zapisovanie, najvyssia uroven spolahlivost, zvycajne predvoleny rezim

#### Instalacia technologie DRBD v systeme OpenSUSE 15.3:
 - instalujeme: `$ sudo zypper -n in drbd drbd-utils drbdmanage`
 - je potrebne mat nasjkor *volnu particiu na oboch uzloch*, ktora sa bude pouzivat, doporucene je LVM2
 - na test sa da vytvorit napr. *virtual-disk* v roznych hypervizoroch (VMw, VBox, KVM-Qemu, ...)
 - dalej vytvorime tzv. *resource file*, nazov napr. `/etc/drbd.d/drbd0.res`, do ktoreho vlozime:
```
resource drbd0 {
    volume 0 {
        device           /dev/drbd0 minor 0;
        disk             /dev/sdb;
        meta-disk        internal;
    }
    on lpic3-suse1 {
        node-id 0;
        address          ipv4 192.168.255.11:7676;
    }
    on lpic3-suse2 {
        node-id 1;
        address          ipv4 192.168.255.12:7676;
    }
    connection-mesh {
        hosts lpic3-suse1 lpic3-suse2;
        net {
            protocol       C;
        }
    }
    net {
        cram-hmac-alg    sha1;
        shared-secret    drbd.2022;
    }
}
```
 - tato konfiguracia *MUSI* byt na oboch uzloch *ZHODNA*
 - nasledne konfiguraciu overime s: `$ sudo drbdadm dump all`
 - dalej povolime definovany *DRBD TCP* port: `$ sudo firewall-cmd --add-port=7676/tcp --permanent`
 - nasledne restartujeme firewall: `$ sudo firewall-cmd --reload`
 - konfiguraciu firewallu overime s: `$ sudo firewall-cmd --list-all`
 - na uzloch vytvorime nove DRBD zariadenie `/dev/drbd0` prikazom: `$ sudo drbdadm create-md drbd0 `
 - na uzloch nasledne aktivujeme DRBD zariadenie: `$ sudo drbdadm up drbd0`
 - overime s: `$ sudo drbdadm status`
 - na jednom uzle inicializujeme bitovu mapu: `$ sudo drbdadm new-current-uuid --clear-bitmap drbd0/0`
 - uzol `lpic3-suse1` nastavime ako primarny: `$ sudo drbdadm primary --force drbd0`
 - overime s: `$ sudo drbdadm status`
 - dalej mozeme uz vytvorit FS na zariadeni `/dev/drbd0`, napr.: `$ sudo mkfs.btrfs /dev/drbd0`

Poznamka: prikazy na vypisanie informacii o diskoch a particiach: `lsblk`, `blkid`, `lsscsi`

Tip: Ako v Systemd *zapnut* sluzbu *po boote* a zaroven spustit: `$ sudo systemctl enable --now <service>`

### Zaklady prace s Cluster suborovym systemom GFS2 (Global File System):

#### Priprava pre zaklady prace s LVM v Cluster prostredi:
- logicke LV particie sa zvycajne mapuju napr. ako: `/dev/mapper/ubuntu--vg-ubuntu--lv`
- kde je teda *VG (Volume Group)* s nazvom `ubuntu` a *LV (Logical Volume)* s nazvom `ubuntu` 
  - poznamka: je to symbolicky link
- LVM (Logical Volume Management) sa spravuje procesom *Device Mapper*, konf. v: `/etc/lvm/lvm.conf`
  - dalsie informacie v `$ man lvm.conf`
- rozsirenie *cLVM* je pre koncept *Clustered LVM*, umoznuje vytvorit tzv. *Clustered Shared Volume*
- rozsirenie *HALVM* je dostupne na RedHat based systemoch, zabranuje sucasnemu zapisu 2 uzlov
- dolezity proces `clvmd` sluzi na propagaciu zmien dalsim uzlom, novsi proces ako HALVM
  - dalsou poziadavkou je *DLM - Distributed Lock Manager*, znamy aj pod nazvom `controld`
- v cLVM su vsetky VG a LV na zdielanom storage, su *stale* dostupne *vsetkym* uzlom
  - vhodne na Cluster suborove systemy ako je napr. *GFS2*
- v HALVM su VG a LV dostupne v danom case len *jednemu* uzlu z clustera, vhodne na `ext4`, `xfs` , `btrfs`
  - na riadenie dostupnosti particii, pre dany uzol, sa vyuziva *Volume Tagging*, pre RedHat based distra
- alternativa HALVM mimo RedHat systemov je *exclusive LVM*

#### Priprava pred instalaciou GFS2 na RedHat based systemoch (CentOS/Rocky Linux):
- rezim *active/active*, zhoda s normou `POSIX - Portable Operating System Interface`
- pracuje *len* v cluster rieseni
- kazdy uzol ma *svoj vlastny FS journal*
- ostatne uzly clustra zreplikuju journal uzla, ktory zlyhava, po *aplikovani Fencing-u*
- su potrebne technologie *DLM* a *cLVM* na koordinaciu *zamykania suborov (file locking)*
- maximalna podporovana kapacita je *100TiB* (asi uz neaktualne, nemam zatial overene)
- treba vytvorit minimalne 2 LUNy, jeden maly (1 MB) na Fencing a druhy na storage napr. 10GB

- ako v RedHat based distrach vypisat *dostupne repozitare*: `$ sudo dnf repolist all`
- verzia pre *CentOS 9 Stream*:
- zapneme repozitare: `$ sudo dnf config-manager --set-enabled highavailability,resilientstorage`
  - instalacia: `$ sudo dnf -y in fence-agents-scsi lvm2-lockd gfs2-utils dlm`

- verzia pre *Rocky-Linux 8.5*:
- zapneme repozitare: `$ sudo dnf config-manager --set-enabled ha,resilient-storage`
  - instalacia: `$ sudo dnf -y in fence-agents-scsi lvm2-lockd gfs2-utils dlm`

- Tip: Prepisanie *zaciatku*, teda aj FS disku nulami: `$ sudo dd if=/dev/zero of=/dev/sda bs=1M count=100`
- Tip: Ako v RedHat based OS zistit, ktory balik poskytuje dany *prikaz*, napr.: `$ dnf provides showmount`

### Priklad na WebServer Cluster pomocou Pacemaker a GFS2 na OS Rocky Linux 8.5:
 - vytvorime DNS zaznamy jednotlivych uzlov, alebo v LABe definujeme `/etc/hosts`
 - na uzloch zapneme repo.: `$ sudo dnf config-manager --set-enabled ha,resilient-storage`
 - na uzloch instalujeme: `$ sudo dnf -y in pacemaker pcs fence-agents-scsi iscsi-initiator-utils`
 - na uzloch zapneme PCS daemona: `$ sudo systemctl enable --now pcsd`
 - na uzloch nastavime heslo pre `hacluster` uzivatela: `$ sudo passwd hacluster`
   - alebo s: `$ sudo echo <heslo> | sudo passwd --stdin hacluster`
 - na uzloch povolime na fwl.: `$ sudo firewall-cmd --add-service=high-availability --permanent`
   - na uzloch restart fwl.: `$ sudo firewall-cmd --reload`
 - na uzloch autentifikujeme clenov/uzly clustra: `$ sudo pcs host auth <hostname1> <hostname2>`
 - na 1 uzle vytvorime cluster: `$ sudo pcs cluster setup rocky_cluster <hostname1> <hostname2>`
 - na 1 uzle nastartujeme cluster(clustre): `$ sudo pcs cluster start --all`
 - na 1 uzle zapneme cluster(clustre): `$ sudo pcs cluster enable --all`
   - overime s: `$ sudo pcs status --full` a s: `$ sudo pcs status corosync`
 
 - poznamka: da sa pouzivat aj Web rozhranie na pracu Pacamaker clustra:
   - povolime na fwl.: `$ sudo firewall-cmd --add-port=2224/tcp --permanent `
   - restartujeme firewall.: `$ sudo firewall-cmd --reload`
   - pripojime sa na `https://nodeX:2224` a prihlasime sa s uzivatelom `hacluster`
 
 - na uzloch zapneme *STONITH/Fencing* s: `$ sudo pcs property set stonith-enabled=true`
   - overime s: `$ sudo pcs property config`
 
 - Fencing/STONITH je rieseny cez *iSCSI LUN*, staci mala velkost 1 MB (mne fungovalo):
 - oba uzly pripojime na LUN, definujeme iSCSI initiatora v `/etc/iscsi/initiatorname.iscsi`
 - pridame IQN, ktore je na iSCSI targete, `InitiatorName=iqn.2022-03.lpic3.lab:gfs.node1.init1`
   - na druhy uzol, napr.: `InitiatorName=iqn.2022-03.lpic3.lab:gfs.node2.init1`
   - podla iSCSI Target-u, nastavime meno/heslo/parametre v subore `/etc/iscsi/iscsid.conf`:
```
        node.session.auth.authmethod = CHAP
        node.startup = automatic
        node.session.auth.username = <meno>
        node.session.auth.password = <heslo>     
```
 - poznmaka: preskumat/otestovat ine auth. algoritmy ako (zranitelne) MD5
 - spustime *iSCSI target discovery* s: `$ sudo iscsiadm -m discovery -t sendtargets -p <storage-Host>`
 - ak najde viac targetov, mazeme zmazat tie, ktore nepotrebujeme:
   - prikaz: `$ sudo rm -rf /var/lib/iscsi/nodes/iqn.2022-03.lpic3.suse1\:target1/`
   - alebo sa mozeme prihlasit na konkretny iSCSI Target s jeho IQN, napr.:

`$ sudo iscsiadm -m node --targetname iqn.2001-05.com.lab:test --portal 192.168.255.100:3260 --login`
 
- prihlasime sa na iSCSI target: `$ sudo iscsiadm -m node --login`
  - overime napr. s: `$ sudo iscsiadm -m session -o show` / `$ sudo lsscsi` / `$ sudo lsblk`
  - dalej si zistime WWN spominaneho 1MB Fencing LUNu: `$ sudo ls -l /dev/disk/by-id/ | grep wwn`
  - nasledne vytvorime Fencing zdroj, treba pouzit prikaz s vlastnym WWN, ktore sme nasli
  - na definiciu clenov clsustr-a treba pouzit DNS hostnames uzlov:

```bash
    $ sudo pcs stonith create scsi-Fence fence_scsi pcmk_host_list="<node1> <node2>" \
    devices=/dev/disk/by-id/wwn-0x600140520845b9b2586439fa1949df69 meta provides=unfencing
```
   - overime s: `$ sudo pcs status --full`
   - mimo produkcie mozeme Fencing otestovat s: `$ sudo pcs stonith fence <node2>`
     - na obnovenie treba druhy uzol rebootovat (nic lepsie som zatial nenasiel)

 - pokracujeme konfiguraciou *active/active storage clustr-a*, postaveneho na *GFS2*
   - podobne ako pri STONITH sa pripojime na dalsi novy LUN, ktory sluzi uz ako aplikacny storage
   - na oboch uzloch upravime konfiguraciu LVM v subore `/etc/lvm/lvm.conf`
     - upravit riadok na: `use_lvmlockd = 1`
     - overime s: `$ sudo lvmconfig | grep lvmlockd`
   - upravime konfiguraciu technologie Quorum: `$ sudo pcs property set no-quorum-policy=freeze`
     - overime s: `$ sudo pcs property config`
   - vytvorime DLM (Distributed Locking Manager) zdroj:
```bash
        $ sudo pcs resource create dlm ocf:pacemaker:controld op monitor interval=30s \
        on-fail=fence --group locking
```
   - dalej zdroj klonujeme na ostatne uzly: `$ sudo pcs resource clone locking interleave=true`
   - pokracujeme vytvorenim zdroja *LVM lockd*:
```bash
     $ sudo pcs resource create res_lvmlockd ocf:heartbeat:lvmlockd \
     op monitor interval=30s on-fail=fence --group locking
```
   - overime s: `$ sudo pcs status --full`
   - *LEN na 1 uzle vytvorime*, na zdielanom iSCSI LUNe particiu so suborovym systemom LVM:
     - disk(y) najdeme s: `$ sudo lsscsi` alebo s: `$ sudo lsblk`
```bash
       $ sudo parted --script /dev/sda "mklabel gpt"
       $ sudo parted --script /dev/sda "mkpart primary 0% 100%"
       $ sudo parted --script /dev/sda "set 1 lvm on"
```
   - sposobov na vytvorenie LVM particie je viac (`fdisk`, `cfdisk`, ...)
   - overime napr. s: `$ sudo fdisk -l /dev/sda`
   - dalej zaradime tzv. *PV (Psysical Volume)* do LVM stacku: `$ sudo pvcreate /dev/sda1`
   - vytvorime zdielanu *VG (Volume Group)* s: `$ sudo vgcreate --shared vg_gfs2 /dev/sda1`
   - po tomto kroku je to "funky", ja som musel restartovat druhy uzol, aby nasiel nove *PV a VG*
     - zatial nepoznam dovod, skusal som `$ sudo pvscan` a `$ sudo vgscan`, ale nepomohlo
     - na oboch uzloch overime stav zdielaneho LVM: `$ sudo vgs; echo; sudo pvs`
       - treba, aby *oba uzly videli PV a VG zo zdielaneho iSCSI storage LUNu*

   - POZOR *LEN* na *inom* uzle upravime vytvorenu VG: `$ sudo vgchange --lock-start vg_gfs2`
   - vratime sa, *LEN* na uzle 1 pokracujeme s novym LV: `$ sudo lvcreate -l 100%FREE -n lv_gfs2 vg_gfs2`
   - dalej vytvorime na *LV (Logical Volume) clusterovy subory system GFS2* s:
     - prikaz: `$ sudo mkfs.gfs2 -j2 -p lock_dlm -t ha_cluster:gfs2-01 /dev/vg_gfs2/lv_gfs2`
     - rozbor: parameter `-j2` urcuje pocet uzlov/zurnalov, dalsi parameter `-t <nazov_clustra>:gfs2-01`
     - kde nazov clustra ziskame z: `$ sudo pcs status`
   - stale na *PRVOM* uzle vytvorime storage zdroj/resource:
```bash
     $ sudo pcs resource create shared_lv ocf:heartbeat:LVM-activate \
     lvname=lv_gfs2 vgname=vg_gfs2 activation_mode=shared vg_access_mode=lvmlockd --group shared_vg
```
   - tento zdroj klonujeme na dalsie uzly: `$ sudo pcs resource clone shared_vg interleave=true`
   - pridame poradie startu: `$ sudo pcs constraint order start locking-clone then shared_vg-clone`
   - spolu start na 1 node: `$ sudo pcs constraint colocation add shared_vg-clone with locking-clone`
   - overime s: `$ sudo pcs status --full` a `$ sudo pcs constraint config`

   - na oboch uzloch vytvorime adresar, kde si cluster "namountuje" GFS2: `$ sudo mkdir /mnt/gfs2disk1`
   - vytvorime zdielany GFS2 zdroj, na ukladanie dat so synchronizaciou:
```bash
    $ sudo pcs resource create shared_fs ocf:heartbeat:Filesystem device="/dev/vg_gfs2/lv_gfs2" \
    directory="/mnt/gfs2disk1" fstype="gfs2" options=noatime op monitor \
    interval=10s on-fail=fence --group shared_vg
```
   - overime cluster stack: `$ sudo pcs status --full`
   - ak je vsetko aktivne bez chyb, vsetky uzly budu mat dostupny GFS2 "mount": `$ sudo df -hT`
   - da sa otestovat, ze napr. kazdy uzol zapise do `/mnt/gfs2disk1` napr. `$ sudo touch uzol1`
     - ostatne uzly uvidia subor `uzol1` v `/mnt/gfs2disk1`

 - pokracujeme riesenim weboveho servera Apache2 ako clustrovy zdroj:
   - najskor riesenie pre data storage, pridame dalsi LUN na iSCSI storage systeme
   - na uzloch pouzijeme tzv. *iSCSI target rescan* s: `$ sudo iscsiadm -m node --rescan`
   - novy LUN overime napr. s: `$ sudo lsscsi` alebo s: `$ sudo lsblk`
   - do LVM zaradime novy iSCSI disk (moze sa pouzit aj disk bez part.): `$ sudo pvcreate /dev/sdc`
   - na uzle 1 vytvorime *zdielanu LVM VG* s: `$ sudo vgcreate --shared vg_web_clus /dev/sdc`
   - na uzle 2 pokracujeme zapnutim LVM Locking-u: `$ sudo vgchange --lock-start vg_web_clus`
   - vratime sa na uzol 1 a vytvorime LV s: `$ sudo lvcreate -l 100%FREE -n lv_web_clus vg_web_clus`
     - na oboch uzloch overime prikazom: `$ sudo vgs` a `$ sudo lvs`, musia vidiet to iste
   - dales na novom zdielanom cluster LV vytvorime suborovy system GFS2: 
```bash
     $ sudo mkfs.gfs2 -j2 -p lock_dlm -t rocky_cluster:web_clus /dev/vg_web_clus/lv_web_clus
```
   - vytvorime cluster LVM zdroj pre WebServer:
```bash
    $ sudo pcs resource create lv_web_shared ocf:heartbeat:LVM-activate lvname=lv_web_clus \
    vgname=vg_web_clus activation_mode=shared vg_access_mode=lvmlockd --group shared_vg
```
   - overime napr. s: `$ sudo pcs status --full`
 
   - dalej instalujeme Apache2 Web Server : `$ sudo dnf -y in httpd`
     - po instalacii si zatial nevsimame stav procesu, *chceme aby ho riadil Pacemaker*, nie "SystemD"
   - na uzloch vytvorime *Server Status* konfig.: `$ sudo vim /etc/httpd/conf.d/server-status.conf`
     - vlozime konfiguraciu:
```apache
    <Location /server-status>
        SetHandler server-status
        Require local
    </Location>
```

   - dalej na uzloch upravime konfiguraciu procesu *Log Rotate* v `/etc/logrotate.d/httpd` na:
      - zakomentujeme povodny riadok, aby `systemd` neriadil proces, ale aby ho riadil *Pacemaker*
```
/var/log/httpd/*log {
    missingok
    notifempty
    sharedscripts
    delaycompress
    postrotate
        #/bin/systemctl reload httpd.service > /dev/null 2>/dev/null || true
        /usr/sbin/httpd -f /etc/httpd/conf/httpd.conf -c "PidFile /var/run/httpd/httpd.pid" -k graceful > /dev/null 2>/dev/null || true
    endscript
}
```
 - na fwl. povolime porty HTTP a HTTPS: `$ sudo firewall-cmd --add-service={http,https} --permanent`
 - restart fwl. s: `$ sudo firewall-cmd --reload`
 - konfiguraciu firewallu overime s: `$ sudo firewall-cmd --list-all`
 - na jednom uzle vytvorime docasny adresar, napr.: `$ sudo mkdir mkdir /mnt/webdisk1/`
 - dalej na uzle docasne "namountujeme" GFS2 particiu na vytvoreny adresar: 
 - prikaz: `$ sudo mount /dev/vg_web_clus/lv_web_clus /mnt/webdisk1/`
 - pokracujeme skopirovanim adresarovej struktury WebServera na zdielanu GFS2 particiu:
   - prikaz: `$ sudo cp -pR /var/www/* /mnt/webdisk1/`
 - pokracujeme vytvorenim jednoduchej testovacej HTTP stranky:
   - prikaz: `$ sudo echo "Testovaci Apache2 WebServer Cluster" > /mnt/webdisk1/html/index.html`
   - dalej "odmountujeme" GFS2 particiu: `$ sudo umount /mnt/webdisk1/`
 - pokracujeme vytvorenim Cluster FS zdroja pre Apache2 WebServer v Pacemaker-y:
```bash
$ sudo pcs resource create web_fs ocf:heartbeat:Filesystem device=/dev/vg_web_clus/lv_web_clus \
  directory=/var/www fstype=gfs2 options=noatime op monitor interval=10s \
  on-fail=fence --group shared_vg
```
 - overime napr. s: `$ sudo pcs status --full`
 - dalej vytvorime virutalnu IP adresu pre zdroj WebServera
```bash
$ sudo pcs resource create apache2_vip IPaddr2 ip=192.168.255.29 cidr_netmask=24 --group apache2grp
```
 - definujeme pravidlo postupnosti startu storage zdrojov pred aplikacnymi zdrojmi: 
   - prikaz: `$ sudo pcs constraint order start shared_vg-clone then apache2grp`
 - pokracujeme vytvorenim samotneho Apache2 zdroja:
```bash
$ sudo pcs resource create apache2_srv ocf:heartbeat:apache configfile=/etc/httpd/conf/httpd.conf \ 
  statusurl=http://127.0.0.1/server-status --group apache2grp
```
 - overime napr. s: `$ sudo pcs status --full`
   - pripadne aj s: `$ sudo pcs resource config`
 - po vytvoreni zdroja `apache2_srv` obnovime *SELinux kontexty* s: `$ sudo restorecon -R /var/www`

 - na zaver otestujeme funkcnost, napr. s klientom: `$ curl http://192.168.255.29/index.html`
   - je vhodne otestovat aj vypadky aktivneho uzla, aka je odolnost clustr-a:
   - napr. s: `$ sudo pcs node standby <hostname_uzolX>`
   - cluster sa samozrejme da vybudovat na viac ako 2 uzloch a je to aj *doporucovane*
   - server Apache2 ma dalsie dolezite nastavenia, ale tu sa im nevenujem

### NFS Server v Cluster rieseni na Rocky Linux 8.5, so zdielanym LVM cez iSCSI:
- na instalaciu pouzijeme novy iSCSI LUN, ktory si vytvorime na storage 
  - novy LUN na cluster uzloch najdeme s: `$ sudo iscsiadm -m node --rescan`
  - overime napr. s: `$ sudo lsscsi` alebo `$ sudo lsblk`
  - poznamka: ako vypisat statistiky danej iSCSI session: `$ sudo iscsiadm -m node -s`
- dalej na oboch uzloch pripravime zdielane LVM, upravime subor: `/etc/lvm/lvm.conf`:
  - riadok `system_id_source = "none"` upravime na `system_id_source = "uname"`
- novy LUN pridame do LVM s: `$ sudo pvcreate /dev/sdX`
- dalej pridame tento disk do VG `vg_ha_lvm` s: `$ sudo vgcreate vg_ha_lvm /dev/sdX`
- overime s: `$ sudo vgs -o+systemid`
  - vo vypise musi byt *System ID* zhodne s vypisom: `$ uname -n`
- z novej VG vytvorime nove LV `lv_ha_lvm` s: `$ sudo lvcreate -l 100%FREE -n lv_ha_lvm vg_ha_lvm`
- na novom LV vytvorime particiu XFS s: `$ sudo mkfs.xfs /dev/vg_ha_lvm/lv_ha_lvm`
- dalej deaktivujeme VG, aby ju mohol spravovat Pacemaker s: `$ sudo vgchange vg_ha_lvm -an`
- na *ostatnych* uzloch "najdeme" nove PV: `$ sudo pvscan --cache --activate ay`
- dalej na uzle 1 vytvorime zdielany LVM zdroj prikazom:
```bash
$ sudo pcs resource create lvm_shared ocf:heartbeat:LVM-activate vgname=vg_ha_lvm \
  vg_access_mode=system_id --group nfs_server_grp
```

- overime stav clustra a LVM zdroja s: `$ sudo pcs status --full`
  - poznamka: ja som si spravil BASH alias: `alias pcf='sudo pcs status --full'`

- pokracujeme instalaciou NFS servera v Pacemaker clustry, na uzloch povolime sluzby na FWL:
```bash
$ sudo firewall-cmd --add-service={nfs,nfs3,mountd,rpc-bind} --permanent
$ sudo firewall-cmd --reload
```

- firewall overime s: `$ sudo firewall-cmd --list-all`
- na uzloch vytvorime adresar pre NFS server: `$ sudo mkdir /home/nfs-server`

- vytvorime cluster zdroj typu *Filesystem* pre HA-NFS server:
```bash
$ sudo pcs resource create nfs_server ocf:heartbeat:Filesystem device=/dev/vg_ha_lvm/lv_ha_lvm \
  directory=/home/nfs-server fstype=xfs --group nfs_server_grp
```

- overime stav a konf. zdroja: `$ sudo pcs status --full" a "$ sudo pcs resource config nfs_server`
- na uzle, kde bezi tento FS zdroj, mozeme overit stav particie: `$ sudo df -hT /home/nfs-server`
- pri chybe mozeme zmenit konf.: `$ sudo pcs resource update nfs_server directory=/home/nfs-XYZ`
- pokracujeme vytvorenim NFS daemon zdroja:
```bash
$ sudo pcs resource create nfs_daemon ocf:heartbeat:nfsserver \
  nfs_shared_infodir=/home/nfs-server/nfsinfo nfs_no_notify=true --group nfs_server_grp
```

- vytvorime cluster virtual-IP, na ktorej bude dostupny zdroj HA-NFS:
```bash
$ sudo pcs resource create nfs_vip ocf:heartbeat:IPaddr2 ip=192.168.255.28 cidr_netmask=24 \
   --group nfs_server_grp
```

- dalej vytvorime zdroj pre NFS notifikacie:
```bash
$ sudo pcs resource create nfs_notify ocf:heartbeat:nfsnotify source_host=192.168.255.28 \
  --group nfs_server_grp
```

- overime stav a konf.: `$ sudo pcs status --full` a `$ sudo pcs resource config nfs_server_grp`

- dalej na *aktivnom* NFS uzle upravime `exportfs` nastavenia, vytvorime zdielany adresar:
  - prikaz: `$ sudo mkdir -p /home/nfs-server/nfs-root/share1`

- dalej na *aktivnom* NFS uzle vytvorime Pacemaker cluster zdroje pre NFS `exportfs`:
  - inak napisane, vytvarame dva rozne NFS exporty v *HA rieseni*
  - *POZOR* na parametre `clientspec=`, `directory=` a `fsid=`
```bash
$ sudo pcs resource create nfs_root_exp ocf:heartbeat:exportfs \
  clientspec=192.168.255.0/255.255.255.0 options=rw,sync,no_root_squash \
  directory=/home/nfs-server/nfs-root fsid=0 --group nfs_server_grp

$ sudo pcs resource create nfs_share1_exp ocf:heartbeat:exportfs \
  clientspec=192.168.255.0/255.255.255.0 options=rw,sync,no_root_squash \
  directory=/home/nfs-server/nfs-root/share1 fsid=1 --group nfs_server_grp
```

- overime stav a konf.: `$ sudo pcs status --full` a `$ sudo pcs resource config nfs_server_grp`
- na tomto uzle nove NFS exporty overime s: `$ sudo showmount -e`
- na testovanie sa mozeme s NFS klietom pripojit na vyexportovane suborove systemy:
  - poznamka: na Rocky Linux 8.5 bolo potrebne instalovat: `$ sudo dnf -y in nfs-utils.x86_64`
  - pripojenie protokolom NFSv4: `$ sudo mount -t nfs4 192.168.255.28:share1 /mnt/nfs`
  - overime s: `$ df -hT /mnt/nfs`
  - pre NFSv3 prikaz: `$ sudo mount -t nfs 192.168.255.28:/home/nfs-server/nfs-root/share1 /mnt/nfs`

Zaklady konceptu *Load-Balancing* v Cluster prostredi OS GNU/Linux
----------------

### Praca s Load-Balancingom, teda rozkladanim zataze na viacero aplikacnych uzlov:
 - zakladne metody Load Balancing-u: 
 - *DNS Round Robin* - velmi jednoduche, nema vsak ziadne monitorovanie dostupnosti uzlov
 - *LVS* - load-balancing na urovni Linux Kernel-u, obmedzene v porovnani s HAProxy/Pacemaker/Corosync
 - *HAProxy* - high-level load balancing, ktory pracuje na 4. (TCP) alebo 7. (HTTP[S]) verstve OSI
   - rozsirene riesenie, podporuje SSL, kompresiu, is-alive-check, pokrocile logovanie
   - najcastejsia aplikacia je v mode Layer7 HTTP[S]
   - HAProxy vyuziva LB algoritmi: *Roundrobin, Lastconn, Source*
   - *Roundrobin*: kazde nove pripojenie je posielane na obsluzenie dalsim app. serverom
   - *Lastconn*: nove pripojenie obsluzene app. serverom s najmensim poctom aktivnych pripojeni
   - *Source*: zdrojova IP klinta je hash-ovana, aby bol pouzity rovnaky app. server na dalsie requesty
 - *Keepalived*: implemetacia VRPP protokolu pre OS GNU/Linux, vytvori virtualnu IP adresu
   - da sa nakonfigurovat "do kriza", s rozdielnymi subnetmi, na primitivny state-less Load Balancing 
   - da sa vyuzit napr. ako redundancia pre *2xHAProxy* na virtualnej IP, alternativa je *Pacemaker*

#### Zjednoduseny priklad instalacie load-balancera HAProxy na OS Rocky Linux 8.5:
 - vyuzijeme 3 servery/VM, kde uzol 3 bude HAProxy LB a zvysne uzly 1+2 budu app/backend servery
 - IP konfig. uzlov, `uzol1:192.168.255.21/24`, `uzol2:192.168.255.22/24`, `uzol3:192.168.255.23/24`
   - samozrejme doporuceny dizajn je L3 routed, netraba zabudnut zapnut IP/IPv6 forwarding v *Kerneli*
 - na uzloch 1 a 2 instalujeme HTTP app/backend server `$ sudo dnf -y install nginx`
 - po isntalacii upravime konf. subor `/etc/nginx/nginx.conf` nasledujuco:
   - riadok `server_name www.srv.world;` na `server_name app.node1.lab;`
   - resp. pre uzol 2 na: `server_name app.node2.lab;`

 - aktivujeme start sluzby NGINX po reboote: `$ sudo systemctl enable --now nginx`
     - overime s: `$ sudo systemctl status nginx`
   - pridame pravidlo na firewall: `$ sudo firewall-cmd --add-service=http --permanent`
     - restartujeme firewall: `$ sudo firewall-cmd --reload`
   - na uzloch 1 a 2 dalej vo web-root adresary `/usr/share/nginx/html` na test zmenime `index.html`
```bash
    $ sudo cd /usr/share/nginx/html
    $ sudo mv index.html index.html.bak
    $ sudo echo "Testovaci uzol 1: app.node1.lab" > index.html
```

 - resp. pre uzol 2: `$ sudo echo "Testovaci uzol 2: app.node2.lab" > index.html`
   - aby sme mohli identifikovat, ktorym backend uzlom bol request vybaveny
 - pokracujeme instalaciou *HAProxy frontend LB* na uzle 1: `$ sudo dnf -y in haproxy`
 - upravime konfig. HAProxy `/etc/haproxy/haproxy.cfg` pridame napr. nasledovne:
```
# moje definicie HAProxy Frontend a Backend
#
# defininica frontend-u

frontend cust1-http-in-FE
    # listen 80 port
    bind *:80
    # set default backend
    default_backend    backend_servers
    # send X-Forwarded-For header
    option             forwardfor

# defininica backend-u

backend backend_servers
    # balance with roundrobin
    balance            roundrobin
    # define backend servers
    server             uzol1 192.168.255.21:80 check
    server             uzol2 192.168.255.22:80 check
```

 - aktivujeme HAProxy sluzbu po reboote: `$ sudo systemctl enable --now haproxy`
 - pridame pravidlo na firewalle pre HAProxy: `$ sudo firewall-cmd --add-service=http --permanent`
     - restartujeme firewall: `$ sudo firewall-cmd --reload`
 - na uzitocnejsie logovanie z HAProxy, upravime konfiguraciu `/etc/rsyslog.conf` nasledovne:
   - odkomentujeme riadky, ktore povolia UDP RSyslog logovanie:
```
    module(load="imudp") # needs to be done just once
    input(type="imudp" port="514")
```

   - dalej pridame riadok: `$AllowedSender UDP, 127.0.0.1`
   - upravime riadok `*.info;mail.none;authpriv.none;cron.none   /var/log/messages`
     - uprava na: `*.info;mail.none;authpriv.none;cron.none;local2.none   /var/log/messages`
   - dalej pridame riadok: `local2.*    /var/log/haproxy.log`
     - umozni logovanie, mozeme napr. sledovat s: `$ sudo tail -f /var/log/haproxy.log`
   - na zaver restartujeme logovaciu sluzbu: `$ sudo systemctl restart rsyslog`
  - rozkladanie zataze overime pripojenim na *LB TCP port 80*, browserom alebo curl-om

Praca s *virtualizacnymi nastrojmi* pre OS GNU/Linux
---------------
- zakladne koncepty: virtualizacia vie *delit fyzicke vypoctove zdroje na viacero oddelenych casti*
  - teda uzmonuje "bezat" *viacero virtualnych pocitacov na spolocnom zdielanom HW*
  - tzv. *Hypervizor* alebo aj *VMM - Virtual Machine Monitor* spravuje a monitoruje virtualizaciu 
  - virtualizovane zdroje tvoria tzv.: *Core 4* skupinu: `procesor, pamat, ulozisko, siet`

Poznamka: ako pridat do LVM predtym pouzivane zariadenie, treba pouzit: `$ sudo wipefs -a /dev/sdb`
 - *POZOR*, prikaz odstrani FS z pouzivaneho disku
 - inak LVM moze hlasit chybu: `Device /dev/sdX excluded by a filter.`
 - prikazy LVM sa daju ciastocne debugovat, napr.: `$ sudo pvcreate -vvv /dev/sdb`

### Praca s virtualizacnou platformou Xen:
- baliky boli z RHEL a klonov odstranene, treba pridat repozitar
- tento postup je instalacia na *OS Debian 11*
- na *Host* systeme instalujeme balik LVM2: `$ sudo apt install lvm2`
- dalej napr. z dvoch diskov spravime LVM2 VG `vgxen`, na instalaciu virtualizovanych systemov:
```bash
$ sudo pvcreate /dev/sdb
$ sudo pvcreate /dev/sdc
$ sudo vgcreate vgxen /dev/sdb /dev/sdc
```

- dalej instalujeme sietove balicky: `$ sudo apt install ifupdown bridge-utils`
- upravime subor `/etc/network/interfaces` nasledovne:
```
# Definicia loopback interface
auto lo
iface lo inet loopback

# Zakomentujeme fyzicku NIC, ktora bude patrit do "xenbr0"

#auto ens33
#iface ens33 inet static
########################
# Definujeme "bridge-interface" s povodnou IP konf. z rozhrania "ens33"
auto xenbr0
iface xenbr0 inet static
bridge_ports ens33
address 192.168.255.246
network 192.168.255.0
netmask 255.255.255.0
broadcast 192.168.255.255
gateway 192.168.255.1
dns-nameservers 193.17.47.1 185.43.135.1 
```

- nasledne restartujeme `networking` sluzbu: `$ sudo systemctl restart networking.service`
  - podla vypisu `$ ip address` by mal byt povodny staticky IP conf. na novom `xenbr0` iface
- instalujeme nastroje a kernel Hypervizora *Xen* s: `$ sudo apt install xen-system-amd64`
- ak je instalcia uspesna, restartujeme Host-a a v Boot-menu vyberieme moznost *Xen Hyperisor*
- dalej pouzivame nastroj `xl`, ktory je tzv. "tool stack" na pracu s Hypervizorom Xen:
  - vypiseme aktivne domeny: `$ sudo xl list`
  - informacia o Host-e ziskame s: `$ sudo xl info`
  - real-time sledovanie hypervizora: `$ sudo xl top`
    - alebo s: `$ sudo xentop`
- aby vzdy Host system bootoval s Xen kernelom, upravime konf. `/etc/default/grub` nasledovne:
  - riadok `GRUB_DEFAULT=0` upravime na:
  - spravnu hodnotu najdeme v subore `/boot/grub/grub.cfg`, hladame string `Xen`

`GRUB_DEFAULT="Debian GNU/Linux, with Xen 4.14-amd64.efi and Linux 5.10.0-13-amd64"`

- aplikujeme novu konf. s: `$ sudo update-grub`
- dalej pridame riadok, ktory zabezpeci minimalne prostriedky pre Xen kernel:

`GRUB_CMDLINE_XEN_DEFAULT="dom0_max_vcpus=1 dom0_mem=1024M,max:1024M"`

- a znova aktualizujeme GRUB2 s: `$ sudo update-grub`
- nasledne restartujeme Host system, napr. s: `$ sudo reboot`
- konfiguraciu overime spravanim menu v GRUB2 a po starte systemu s: `$ sudo xl list`
  - domena `Domain-0` by mala mat obmedzene zdroje podla konfiguracie z *GRUB-u*

- hlavna konfiguracia Xen-u sa nachadza v adresary `/etc/xen/`
  - na konfiguraciu *HVM (Hardware Virtual Machine)* sa da pouzit sablona `/etc/xen/xlexample.hvm`
  - na konfiguraciu *PV (Para-Virtualization)* sa da pouzit `/etc/xen/xlexample.pvlinux`
  - globalny konf. subor je: `/etc/xen/xl.conf`
  - v adresari `/etc/xen/scripts/` su skripty, ktore sa vyuzivaju na pracu s *Xen*
  - subor `/etc/default/xen` umoznuje nastavit predvoleny *Tool Stack* pre Xen
    - bez konfiguracie je predvoleny Tool Stack program `xl` postaveny na kniznici *Xen Light*
      - dalsie informacie napr. v: `$ man xl`
  - dalsi subor `/etc/default/xendomains` definuje spravanie VMs po reboote Host-a
  - adresar s logovacimi udajmi Xen-u je: `/var/log/xen/`
  - systemovy adresar `/var/lib/xen/` uklada uzivatelske data VM instancii

- nasledne instalujeme sadu nastrojov pre Xen: `$ sudo apt install xen-tools`
  - konfiguraciu nastrojov najdeme v subore `/etc/xen-tools/xen-tools.conf`
    - odkomentujeme a upravime riadok `lvm = vg0` na `lvm = vgxen`
  - v adresary `/usr/share/xen-tools/` najdeme typy OS pre Xen VM instancie
 
- nasledne vytvorime zjednodusenu Xen domenu/image:
```bash
$ sudo xen-create-image --hostname=xenvm01 --lvm=vgxen --memory=2G --maxmem=2G --vcpus=2 \
--size=8G --swap=1G --fs=ext4 --dhcp --arch=amd64 --dist=jessie
```

- parameter `memory/maxmem` udava velkost RAM a max. velkost RAM
- parameter `vcpus` udava pocet virt. CPU
- parameter `size` udava velkost disku
- parameter `swap` udava velkost Swap particie
- parameter `fs` udava typ suboroveho systemu
- parameter `dhcp` definuje IP konfiguraciu z DHCP
- parameter `arch` udava procesorovu architekturu
- parameter `dist` udava typ Linux distribucie
- po ukonceni z vypisu ziskame udaje o SSH a heslo `root` uzivatela, ktorym sa prihlasime na VM

- nasledne vytvorime VM instanciu podla vygenerovaneho Image/konfigu:
  - prikaz: `$ sudo xl create /etc/xen/xenvm01.cfg`
  - overime prikazom: `$ sudo xl list`
  - po nabootovani VM instanacie sa mozeme pripojit na jej terminal: `$ sudo xl console xenvm1`
    - z konzoly sa odhlasime skratkou `Ctrl + ]`
  - domenu/VM vypneme s: `$ sudo xl shutdown xenvm01`

#### Priklad ako vytvorit HVM (Hardware Virtual Machine) instanciu s instalacnym `.iso` suborom:
- vytvorime si LV pre novu VM: `$ sudo lvcreate --size 10g --type linear -n lv_fedora35vm01 vgxen`
- podla sablony si v adresari `/etc/xen/` vytvorime konf. subor na vytvorenie VM: 
  - prikaz: `$ sudo cp xlexample.hvm fedora35vm01.cfg`
  - nasldene upravime konf. subor instancie `fedora35vm01.cfg` kde:
    - riadok `name =` upravime na `name = fedora35vm01.cfg`
    - riadok `memory =` upravime na: `memory = 2048`
    - riadok `maxmem =` upravime na: `maxmem = 2048`
    - riadok `vif =` upravime na: `vif = [ 'bridge=xenbr0' ]`
    - riadok `disk =` zmenime napr. na: 

`disk = [ 'phy:/dev/vgxen/lv_fedora35vm01,hda,w','file:/root/fed35-x86_64.iso,hdc:cdrom,r' ]`

  - riadok `sdl = 1` zakomentujeme a odkomentujeme riadok `vnc = 1`
  - dalej pridame riadok, tak aby najskor bootoval *Disk* a potom *CD-ROM image*: 
        boot = "dc"

- vytvorime VM instanciu, na ktoru sa da pripojit VNC protokolom: `$ sudo xl create fedora35vm01.cfg`

- overime prikazom: `$ sudo xl list`

Poznamka: technologia Xen bola davnejsie odkupena spol. Citrix a je to dlhsie komercny produkt
  - z tohto dovodu OSS komunita viac preferuje kombinaciu projetov ako je KVM, QEMU, libvirt...
  - preto tato cast poznamok nepokracuje dalej

### Praca s virtualizacnou platformou *KVM* a pridruzenymi projektami *QEMU* a *libvirt*:
 - *KVM - Kernel based Virtual Machine*, sluzi ako *akcelerator* pre nastroje *QEMU*
 - *QEMU* - genericky emulator a virtualizator pocitacov
 - *KVM+QEMU* podporuju viacero suborovych diskov, ako napr. `raw`, `qcow2`, `vdi`, `vmdk`, ...
   - *qcow2* - QEMU Copy On Write version 2
   - jedine format *qcow2* podporuje *snapshot-y* (neviem ci uz ich nie je viac)

#### Zjednoduseny priklad, ako instalovat KVM + QEMU na Host pocitaci/servery s OS Rocky Linux 8.5:

- overime podporu virtualizacie v CPU (Intel alebo AMD): `$ sudo egrep -o '(vmx|svm)' /proc/cpuinfo`
  - podpora pre Intel je `vmx`, podpora pre AMD je `svm`

- overime pritomnost modulu KVM v kerneli: `$ sudo lsmod lvm`
  - ak nenajde tak: `$ sudo modprobe kvm`
  - a nasledne: `$ sudo modprobe kvm_intel` alebo `$ sudo modprobe kvm_amd`
- overime pritomnost KVM v systeme: `$ sudo ls -al /dev/kvm`
- dalej instalujeme QEMU s podporou KVM: `$ sudo dnf -y in qemu-kvm`
- mozeme uz intalovat aj nastroje/API `libvirt` s: `$ sudo dnf -y in libvirt virt-install`
  - sluzbu `libvirt` nasledne *zapneme* s: `$ sudo systemctl enable --now libvirtd.service`
  - overime stav sluzby: `$ sudo systemctl status libvirtd.service`
- spol. RedHat doporucuje pouzit `libvirt`, ak chceme pouzit `qemu-kvm` je potrebny link do $PATH:
  - prikaz: `$ sudo ln -s /usr/libexec/qemu-kvm /usr/local/sbin/qemu-kvm`

- vytvorime VM disk vo formate qcow2: `$ sudo qemu-img create -f qcow2 /mnt/kvm-stor/qemu.vm01.img 10G`
- dalej vytvorime samotnu VMm ku ktorej pripojime instalacny .ISO image s OS Fedora 35:
  - instancia bude bezat na pozadi s dostupnym VNC pripojenim

```bash
$ sudo qemu-kvm -name vm01_kvm -hda /mnt/kvm-stor/qemu.vm01.img \
-cdrom /root/fed35-amd64.iso -boot d -m 2048 &
```

- na test si vytvorime SSH tunnel, ktory prepoji VNC server na porte *localhost:5900* so sietou
  - na tomto *TCP/5900* porte pocuva VNC server pre QUEMU/KVM Host-a, kde mozeme ovladat danu VM
  - prikaz napr. na KVM Host-e: `$ sudo ssh -N -R *:6000:localhost:5900 uzivatel@<KVM-Host>`
    - nasledne sa cez VNC klienta pripojime na adresu <KVM-Host> a TCP port 6000
  - pre viac VM instancii treba rozlisovat cislo VNC Display port-u
    - toto cislo zistime prikazom `$ sudo virsh vncdisplay <nazovVM>`

- dalej mozeme VM instanciu vytvorit aj nastrojom `virt-install` takto:
  - diskovy priestor 8GiB udava parameter `--disk size=8`
  - priblizna varianta OS sa da zistit prikazom: `$ sudo osinfo-query os`

```bash
$ sudo virt-install --name=fedoraVM01 --memory=2048 --vcpus=2 --disk size=8 \
--os-variant=fedora34 --cpu host --cdrom /mnt/kvm-stor/fed35-amd64.iso &
```

- stav VM instancie overime s: `$ sudo virsh list --all`

Dalsie nastroje na pracu s KVM: `qemu-ga`, `qemu-img`, `qemu-kvm`
- nastroj `qemu-ga` umoznuje napr. ziskat info o VM, suspendovat VM, nastavit systemovy cas, ...
- priklad: ako ziskat informacie o qcow2 image: `$ sudo qemu-img info /mnt/kvm-stor/qemu.vm01.img`
- ako otestovat konzistenciu image: `$ sudo qemu-img check /mnt/kvm-stor/qemu.vm01.img`
  - dalsie moznosti: `create`, `commit`, `compare`, `convert`, `map`, `snaphost`, `rebase`, `resize`, `amend`
  - dalsie informacie napr. v: `$ man qemu-img`

Dolezity nastroj `qemu-kvm` je hlavny nastroj pre pracu s QEMU+KVM stackom:
 - tento nastroj ma velke mnozstvo moznosti/nastaveni, treba pozriet napr.: `$ man qemu-kvm`
 - dalsia sucast je interaktivny nastroj *KVM Monitor*, ktory umoznuje riadenie/sledovanie KVM+QEMU
 - nastroj ma predvolene graficke rozhranie, parameter `stdio` aktivuje textove rozhranie
 - v terminale spustime s: `$ sudo qemu-kvm -monitor stdio`
 - prva pomoc je prikaz `help`, dalej napr. ked zadame `info`, vypise nam moznosti prikazu

Tip: Ako sledovat cinnost *sietoveho unit-u* v systemD: `$ sudo journalctl -f -u systemd-networkd`

### Zaklady prace s *OS-level virtualization* projektami *OpenVZ* a *LXC*:
 - tieto projekty pracuju s konceptom tzv. *kontajnerov*
 - dalsia moznost je *Application-level virtualization*, kde je hlavnym zastupcom platforma *Docker*

#### Praca s projektom *OpenVZ*, ktory pracuje s kontajnermi:
 - kontajnery funguju ako standardny linuxovy VPS server, ktory je izolovany od ostatnych instancii
 - *OpenVZ* pouziva modifikovany Kernel, platforma podporuje tzv. *Checkpoit-y* a *Live migraciu*
   - migracia zmrazi/Freeze stav kont. do suboru a na druhom hoste ho "rozmrazi/Unfreeze" a spusti 
 - nova instalacia je riesena cez stiahnutelny ISO image specialnej Linux distribucie s OpenVZ 
 - po instalacii VZ-Linux mozeme vytvorit OS-level kontajner podla preddefinovanej sablony:
   - napr.: `$ sudo prlctl create ubuCT1 --vmtype ct --ostemplate ubuntu-20.04-x86_64`
   - zoznam zakladnych sablon ziskame s: `$ sudo vzpkg list`

Poznamka: pretoze projekt OpenVZ je uz zastarany, poznamky dalej nepokracuju

#### Praca s virtualizacnou platformou *LXC - Linux Containers*:
 - snaha je vytvorit co najefektivnejsi kontajner bez emulacie HW
 - vhodny na vytvaranie *Developer prostredi*, podporuje sablony/Templates
 - vyuziva projekty/technologie: *Namespaces, CGroup, Chroot, Apparmor/SELinux, Seccomp*
 
Zjednoduseny priklad ako na OS Ubuntu 20.04 spustat *neprivilegovane* LXC kontajnery:

 - je vhodne vytvorit noveho uzivatela, ktory nie je sysadmin
 - instalujeme balik nastrojov: `$ sudo apt install lxc`
 - nasledne overime, ci ma aktualny uzivatel mapovanie `subUID` a `subGID` pre LXC
   - kontrolujeme subory `/etc/subuid` a `/etc/subgid`
 - dalej definujeme networking limit pre LXC, umozni pripojit *10 veth NICov* k `lxcbr0` bridgu
   - upravime subor `/etc/lxc/lxc-usernet` a vlozime riadok `<uzivatel> veth lxcbr0 10`
 - vytvorime konf. LXC adresar pre daneho uzivatela: `$ mkdir -p /home/<uzivatel>/.config/lxc`
 - dalej skopirujeme vzorovy konf. subor: `$ cp /etc/lxc/default.conf /home/<uzivatel>/.config/lxc/`
 - nasledne mozeme upravit lokalnu LXC konfiguraciu v subore `default.conf`
   - pridame riadky, podla UID a GID mapovacich suborov, ktore sa kontrolovali, napr.:
```
lxc.idmap = u 0 165536 65536
lxc.idmap = g 0 165536 65536
```

 - je potrebne nastavit premennu: `$ export DOWNLOAD_KEYSERVER="hkp://keyserver.ubuntu.com"`
   - prikaz mozeme vlozit aj napr. do suboru `/home/<uzivatel>/.bashrc`
 - dalej je potrebne restartovat Host system, napr. s: `$ sudo reboot`
 - po reboote mozeme pracovat s kontajnermi, vytvorime kont. podla sablony s nazvom `lxctest1`
   - prikaz: `$ lxc-create -t download -n lxctest1`
   - nasledujeme sprievodcu, kde zadame system, verziu a CPU architekturu
   - napr. sa da zadat minimalisticka distribucia  `alpine` + `3.15` + `amd64` 
 - je potrebne este nastavit prava *execute* na adresar `/home/<uzivatel>/.local`
   - prikaz: `$ chmod og+x .local/`
 - nasledne uz mozeme spustit do pozadia vytvoreny kontajner `lxctest1` s Alpine Linux 3.15
   - prikaz: `$ lxc-start -d -n lxctest1`
   - stav kontajnerov overime s: `$ lxc-ls -f`
   - na konzolu kontajnera sa pripojime s: `$ lxc-attach -n lxctest1`
   - informacie o danom kontajnery: `$ lxc-info -n lxctest1`
   - kont. zastavime s: `$ lxc-stop -n lxctest1`
   - kont. vymazeme, ak je zastaveny, prikazom: `$ lxc-destroy lxctest1`

Poznamka: praca s platformou Docker je uz vyssie popisana v tychto poznamkach

#### Virtualizacny nastroj *VirtualBox*:
 - je to tzv. *hosted hypervisor/Type-2 hypervisor*, ktory sa instaluje ako Aplikacia na OS
 - dalsie informacie: `https://www.virtualbox.org/`

#### Nastroj *Packer* sluzi na automatizovanu tvorbu a konfiguraciu VM imagov:
 - nastroj dalej vyuziva automatizacne projekty *Puppet* a *Chef*
 - dalsie informacie napr.: `https://www.packer.io/`

#### Nastroj *Vagrant* sa vyuziva:
 - na automaticku tvorbu a manazment VM prostredi, ktore su prenositelne
 - nastroj je integrovany s projektami *Puppet*, *Chef* a *Ansible*
 - na definiciu VM prostredi a ich parametrov vyuziva tzv. *VagrantFile*
 - dalsie informacie napr.: `https://www.vagrantup.com/`

### Praca s kniznicou/nastrojmi/API pod nazvom projektu `libvirt`:
 - sluzi na unifikovany manazment virtualnych zdrojov roznych typov (KVM, QEMU, VMware, LXC, Xen, ...)
 - poskytuje CLI nastroje na manazment, ako su napr. `virsh`, `virt-install`, `virt-manger`
 - informacie a konfiguraciu VM instanacii uklada vo *formate XML*
 - casto pouzivane subcommands/sub-prikazy nastroja `virsh` ohladom networkingu:
   - `virsh net-list`: vypise virtualne siete
   - `virsh net-start`: spusti virtualnu siet
   - `virsh net-destroy`: zastavi a vymaze virtualnu siet
   - `virsh net-undefine`: odstrani virtualnu siet, pokial nie je aktivna
   - `virsh net-edit`: uprava XML konfiguracie virtualnej siete
   - `virsh net-dumpxml`: vypise XML konfiguraciu virtualnej siete

 - nastroj `libvirt` vyuziva na manazment uloziska tzv. Storage Pool-y
   - daju sa vyuzit rozne Pool-y: *Filesystem, NFS, Adresar, LVM, Fyz. disk, iSCSI, Gluster, ...*
 - casto pouzivane subcommands/sub-prikazy nastroja `virsh` ohladom storage manazmentu:
   - `virsh pool-build`: vytvori storage pool
   - `virsh pool-define-as`: prida perzistentny storage pool pomocou dalsich CLI parametrov
   - `virsh pool-delete`: vymaze storage pool
   - `virsh pool-destroy`: deaktivuje storage pool
   - `virsh pool-edit`: uprava XML konf. storage pool-u
   - `virsh pool-build`: vytvori storage pool
   - `virsh pool-start`: zapne neaktivny storage pool
   - `virsh vol-create-as`: v storage pool-e vytvori storage volume pomocou dalsich CLI parametrov
   - `virsh vol-delete`: odstrani volume z daneho storage pool-u
   - `virsh vol-list <pool>`: vypise zoznam dostupnych volume-s

#### Praca s VM hosting stackom z komponentov *KVM,  QEMU, libvirt* na OS Rocky Linux 8.5:
 - poznamka: instalacia platformy je uz vyssie popisana v tychto poznamkach
 - adresar `/var/lib/libvirt/images/` je predvolena cesta pre disk image subory
 - adresar `/etc/libvirt/` je uzlozisko pre globalnu konfiguraciu
 - adresar `/etc/libvirt/qemu/` je uzlozisko pre XML konfiguraciu VM intanacii, resp. Domen
   - priama uprava XML suborov nie je doporucena, treba pouzit `virsh edit` a `vrish net-edit`
   - nastroj na jej validaciu, napr: `$ sudo virt-xml-validate /etc/libvirt/qemu/fedora35VM01.xml`

 - podla vyssie uvedenych poznamok si pripravime LVM2 VG skupinu, napr. s nazvom `vg-kvm`
 - pokracujeme vytvorenim storage pool-u s nazvom `lvm_pool`
   - prikaz: `$ sudo virsh pool-define-as lvm_pool logical --source-name vg-kvm --target /dev/vdb1`
   - aktivujeme Pool: `$ sudo virsh pool-start lvm_pool`
   - overime prikazom: `$ sudo virsh pool-list --all`
   - zabezpecime automaticky start: `$ sudo virsh pool-autostart lvm_pool`
   - vytvorime si 2 particie/vulumes: `$ sudo virsh vol-create-as lvm_pool kvm-vol1 10G`
     - resp.: `$ sudo virsh vol-create-as lvm_pool kvm-vol2 10G`
     - overime prikazom: `$ sudo virsh vol-list lvm_pool`
     - kedze, libvirt pracuje s LVM2, tak overime aj prikazom: `$ sudo lvs`

 - Tip: ako deaktivovat libvirt Storage pool s nazvom `lvm_pool` s: `$ sudo virsh pool-destroy lvm_pool`
   - po deaktivacii sa moze Storage pool zmazat: `$ sudo virsh pool-delete lvm_pool`
   - a nasledne aj oddefinovat: `$ sudo virsh pool-undefine lvm_pool`

 - vytvorime VM instanciu s instalaciou Fedora35 z Poolu `lvm_pool` a diskom/volume `kvm-vol1`
   - instanacia ma pridelene *2xvCPU, 2GB RAM, grafika pocuva na VNC servery TCP/5900, display :0*
   - pozor na nastavenie firewallu na Host-e
```bash
$ sudo virt-install \
--virt-type kvm \
--name fedora35VM01 \
--vcpus=2 \
--ram 2048 \
--disk vol=lvm_pool/kvm-vol1  \
--network network=default --graphics vnc,listen=0.0.0.0 \
--noautoconsole \
--cpu host \
--os-type=linux \
--os-variant=generic \
--cdrom=/mnt/fed35-amd64.iso
```

 - stav instalacie VM instancie overime s: `$ sudo virsh list --all`
 - na virtualny monitor instancie sa da pripojit s VNC klientom: `$ vncviewer <Host:diplay>`
 - ako vykonat *gracefull shutdown* VM instancie: `$ sudo virsh shutdown --domain fedora35VM01`
 - ako vykonat *force shutdown* VM instanciu: `$ sudo virsh destroy --domain fedora35VM01`
   - ako vymazat VM instanciu: `$ sudo virsh undefine --domain fedora35VM01`
   - *POZOR* vymaze VM + jej disk: `$ sudo virsh undefine --domain fedora35VM01 --remove-all-storage`

### Praca so sadou virtualizacnych nastrojov pod nazvom projektu *oVirt*:
 - OSS projekt zalozeny spol. RodHat, poskytuje centralny manazment nad zdrojmi pre virtualizaciu
 - dalsie informacie na: `https://www.ovirt.org/`
 - ma webovy interface, podporuje live-migraciu, distribuovany, pouziva KVM, umoznuje Virtualne DC
 - risenie ma tieto komponenty *oVirt Engine*, ktory umoznuje pristup a manzment k *oVirt uzlom*
   - uzly *oVirt Nodes* poskytuju funkciu Host systemu, na ktorom bezia VM instanacie
   - dalsi komponent je datove ulozisko *storage*, ktore moze byt *LocalFS, NFS, iSCSI, Gluster, ...*
   - ulozisko *storage* ma tieto domeny:
     - *Data* - uklada VM disky a OVF sablony/definicie
     - *ISO* - uklada instalacne ISO image

#### Zjednoduseny postup instalacie oVirt prostredia s NFS storage riesenim na OS Rocky Linux 8.5:

 - na LAB pouzijeme 3 servery/uzly s Rocky Linux 8.5, kde treti bude v role NFS storage servera
   - minimalna kapacita LocalFS disku je 25GB a doporucena je 50GB
   - servery/uzly 1 a 2 budu sluzit na manazment a poskytovanie vypoctovych/sietovych zdrojov

 - pokracujeme instalaciou NFS servera na uzle/servery c. 3:
   - instalujeme balicky: `$ sudo dnf -y in nfs-utils`
   - upravime subor `/etc/idmapd.conf`
     -  kde odkomentujeme riadok `Domain = ` a upravime napr. na: `Domain = rock3.example.com`
   - povolime na FWL: `$ sudo firewall-cmd --add-service={nfs,nfs3,mountd,rpc-bind} --permanent`
     - restartujeme FWL: `$ sudo firewall-cmd --reload`
   - vytvorime skupinu `kvm` na prihlasenie *oVirt* clustr-a: `$ sudo groupadd kvm -g 36`
   - vytvorime uzivatela `vdsm` pre oVirt: `$ sudo useradd vdsm -u 36 -g 36 -s /sbin/nologin -M -d /`
   - vytvorime adresar `/var/lib/ovirt-share` a nastavime mu vlastnika a prava:
     - diskovy priestor treba mat pripraveny z *LocalFS, iSCSI, FC, ...*
```bash
$ sudo mkdir -p /var/lib/ovirt-share
$ sudo chown -R vdsm:kvm /var/lib/ovirt-share/
$ sudo chmod 755 /var/lib/ovirt-share
```

   - do suboru `/etc/exports` pridame: `/var/lib/ovirt-share/ 192.168.255.0/24(rw,no_root_squash)`
   - aktivujeme sluzby potrebne pre NFS server: `$ sudo systemctl enable --now rpcbind nfs-server`

 - dalej je potrebne na fyz. uzle 1 instalovat SMTP server, pouzijeme napr. projekt *Postfix*
   - na *Admin node* instalujeme potrebny balik: `$ sudo dnf -y install postfix`
   - nasledne upravime globalnu/hlavnu konfiguraciu v subore `/etc/postfix/main.cf` napr. takto:
```postfix
# moje upravy v LABe:

myhostname = rock1.example.com

mydomain = example.com

myorigin = $mydomain

inet_interfaces = all

inet_protocols = all

mydestination = $myhostname, localhost.$mydomain, localhost, $mydomain

mynetworks = 192.168.255.0/24, 127.0.0.0/8

home_mailbox = Maildir/

smtpd_banner = $myhostname ESMTP

# dalej pridame riadky:

disable_vrfy_command = yes
smtpd_helo_required = yes
message_size_limit = 10240000
```

 - po uprave konf. aktivujeme sluzbu SMTP servera: `$ sudo systemctl enable --now postfix`
   - overime s: `$ sudo systemctl status postfix`
 - povolime SMTP port TCP/25 na FWL: `$ sudo firewall-cmd --add-service=smtp --permanent`
   - restartujeme FWL: `$ sudo firewall-cmd --reload`

 - dalej mozeme pokracovat s instalaciou *oVirt Engine* na *Admin* uzle/servery c.1:
 - pridame repo.: `$ sudo dnf -y in https://resources.ovirt.org/pub/yum-repo/ovirt-release44.rpm `
 - instalujeme potrebne baliky (cca. 230MB): `$ sudo dnf -y install ovirt-hosted-engine-setup`
 - po instalacii spustime instalacny skript: `$ sudo hosted-engine --deploy`
 - skript doporucuje spustit instlaciu v nastroji `tmux`, pripadne `screen`
 - v skripte je potrebne zadavat parametre podla poziadavky, je *treba mat DNS/hosts zaznami*
 - na *Storage subsystem* som pouzil NFSv4 s adresou: `rock3.example.com:/var/lib/ovirt-share`
 - instalaciu overime s: `$ sudo hosted-engine --vm-status`
   - alebo: `$ sudo virsh -c qemu:///system?authfile=/etc/ovirt-hosted-engine/virsh_auth.conf list`
   - po instalacii je dostupne web rozhranie s mng adresou a heslom, ktore sme zadavali do skriptu
     - meno je `admin` a heslo zadane do instalacneho skriptu (`$ sudo hosted-engine --deploy`)
     - na nahranie instalacnych .ISO je volba: `Storage > Disks > vpravo volba "Upload"`
     - mne to zlyhalo kvoli CA certifikatu, po importovani do Firefoxu siel upload OK
     - CA certifikat mal link, suboru som pridal `.pem` a importoval ako CA do Firefoxu v *Nastaveniach*

`http://{engine_url}/ovirt-engine/services/pki-resource?resource=ca-certificate&format=X509-PEM-CA'`

 - Dalsi vypoctovy uzol, teda *oVirt Node/Host* mozeme nainstalovat z pripraveneho .ISO:
   - upravene distro z: `https://resources.ovirt.org/pub/ovirt-4.4/iso/ovirt-node-ng-installer/`
   - je potrebne mat spravne nadefinovane DNS zaznami jednotlivych uzlov, storage, ...
   - inak napisane, treba mat pripraveny aspon zakladny systemovy dizajn
   - na pridanie dalsieho Node/uzla je vhodne vyuzit PKI auth. v SSH, pomocou klucov
   - ked vytvorime VM instanciu a pripojime instalacne ISO, da sa pripojit protokolom *SPICE*
     - na MacOS som pouzil neoficialny balickovaci system *Home Brew* podla: `https://brew.sh/`
     - pridal som *repo* a instaloval: 
```bash
$ brew tap jeffreywildman/homebrew-virt-manager
$ brew install virt-viewer 
```

 - po instalacii som otvoril subor, ktory poskytne oVirt Engine: `$ remote-viewer console.vv`
 - pripojenie je podobne ako VNC, text editorom sa da nahliadnut do suboru `console.vv`
 - je vidiet, ze subor `.vv` ma platnost 120 sekund, potom exspiruje vygenerovane heslo

#### Poznamky k projektu OpenStack:
 - definovany ako *Cloud Operating System*
 - *rozsiahly projekt*, urceny na manazment cloudovych *zdrojov compute, storage, network v datovom centre*
 - na manzment a provisioning zdrojov vyuziva webove dashboard rozhranie a API rozhranie
 - zdroje typu *Compute* mozu byt: *bare metal HW, VMs, kontajnery*
 - zdroje typu *Storage* mozu byt: *Block Device, File Storage, Object Storage*

 - zakladne komponenty: `Horizon, Heat, Nova, Neutron`
   - *Horizon*: webovy interface pre adminov a tenantov
   - *Heat*: komponent na orchestraciu, ktory vyuziva konf. sablony a je integrovany s *Puppet, Chef, ...*
   - *Nova*: - sluzi na provisioning Compute zdrojov (Virtual Machines, Bare Metal HW, Kontajnery)
   - *Neutron*: poskytuje manazment sietovych zdrojov a sluzieb ako *DHCP, DNS, LB, Sec, Routing, ...*
   - *Ironic*: sluzby pre HW provisioning s *PXE, IPMI, iLO, iDRAC, ...*, je integrovany s *Nova/Neutron*
   - *Swift*: *Object storage* sluzba, poskytuje sluzby datoveho uloziska s mensim vykonom, kapacita++
   - *Cinder*: poskytuje sluzby pre *Block Storage* uloziska, ich provisioning a samotne pouzivanie
   - *Keystone*: poskytuje sluzbu identit, teda autentifikacie a autorizacie pre *OpenStack*
   - *Glance*: poskytuje sluzby na pracu s image-mi, ako su `.iso`, `.ovf`, `.vmdk`, `...`
   - projekt *OpenStack* ma vela dalsich sluzieb a sub-projektov, ktore nie su predmetom tychto poznamok
 - dalsie informacie napr. na: `https://www.openstack.org/`

#### Poznamky k projektu CloudStack:
 - je definovany ako OSS produkt na nasadenia a spravu velkych VM prostredi
 - je to full-stack *Infrastructure as a Service (IaaS)* riesenie pre public/private/hybrid cloud
 - zakladne vlastnosti:
   - vysoka skalovatelnost, nasiel som Case Study s viac ako 30 tisic Host servermi
   - open-source vyvoj
   - podpora Compute orchestration
   - podpora NaaS: Network as a Service
   - storage manazment pre VM instancie ako aj pre image a sablony, snapshoty
   - manazment uzivatelov a uctov
   - podpora multi-tenancy
   - nativne *REST API + kompatibilne API s Amazon S3/EC2*
   - uctovanie/accounting vyuzivanych zdrojov
   - webove UI
   - terminalove CLI nastroje
   - dobre relativne *RTTV - Rapid Time To Value*
   - podporuje viacero Hypervizorov, napr.: *VMware, KVM/QEMU, XenServer, HyperV, OVM, UCS, ...*
 - tzv. *Manazment Server* je zodpovedny za orchestraciu zdrojov v Cloud prostredi
   - bezi ako kontajner na platforme *Apache Tomcat*
   - vyzaduje databazu, napr. *MySQL/MariaDB*, pripadne jej Cluster riresenie *Galera MariaDB Cluster*
 - dalsie informacie napr. na: `https://cloudstack.apache.org/`

#### Projekt Eucalyptus:
 - je OSS riesenie pre IaaS platformi, ktore su kompatibilne s Amazon AWS
 - umoznuje vytvorit privatny aj public cloud
 - architektura postavena na GNU/Linux, ktora umoznuje vyuzit svoje vlastne zdroje kompati. s AWS
 - dalsie infomacie napr. na: `https://www.eucalyptus.cloud/`

#### Projekt OpenNebula:
 - kombinuje virtualizaciu a kontajnery na budovanie multi-tenant cloud rieseni
 - umoznuje vybudovat private/public/hybrid cloud riesenia + edge computing
 - komercny produkt s profesionalnou/garantovanou podporou
 - plne automatizovany provisioning a elasticita na poskytovanie on-demand vypoctovych prostriedkov
 - integruje viacero technologii, napr.: *VMware, KVM/QEMU, Firecracker, LXC, Docker, K8S, Terraform*
 - umoznuje nasadit *hybrid/edge* riesenie s vyuzitim externych zdrojov ako *AWS, Google, Equinix*
 - dalsie informacie napr. na: `https://opennebula.io`

Nezaradene poznamky pre system GNU/Linux
---------------

Tip: Ako vypisat vsetky *.dotfile* a *.dotdirectory*, prikaz: `$ ls -ld .??*`

Tip: Ako zalohovat pomocou programu `rsync` vsetky *.dotfile* a *.dotdirectory*:
- prikaz: `$ rsync -av /zdrojova/cesta/.??* /cielova/cesta/`

#### Ako v systeme GNU/Linux vypnut HW PC-speaker:

- prikaz: `$ sudo rmmod pcspkr`

#### Dobra stranka na zaciatocnu konfiguraciu znamych distribucii Linuxu:

    https://www.server-world.info/en/
 
- neviem do kedy bude online a chyba praca s protokolom IPv6 :(

#### Ak system nepreklada DNS zaznami a hlasi: "Temporary failure in name resolution"
 - treba skontrolovat syntax suboru `/etc/resolv.conf`
 - pripadne restartovat DNS resolver proces: `$ sudo systemctl restart systemd-resolved.service`
 - overime s: `$ sudo systemctl status systemd-resolved.service`

#### Ako v Unix-like systemoch konvertovat video kodekom H.265
1. instalujeme nastroj `ffmpeg` (`apt install ffmpeg`, `dnf install ffmpeg`, `brew install ffmpeg` a pod.)

2. podla tohto popisu dame konvertovat:

    >Update 2020: This answer was written in 2009.
    >Since 2013 a video format much better than H.264 is widely available, 
    >namely H.265 (better in that it compresses more for the same quality, or 
    >gives higher quality for the same size). 
    >To use it, replace the libx264 codec with libx265, and push the compression lever further 
    >by increasing the CRF value — add, say, 4 or 6, since
    >a reasonable range for H.265 may be 24 to 30. Note that lower CRF values correspond to 
    >higher bitrates, and hence produce higher quality videos.
    >
    > zdroj: `https://unix.stackexchange.com/a/38380`

- priklad: `$ ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4`

#### Obsah tejto stranky bol vygenerovany BASH skritpom:

- na odkaze: `https://github.com/ekalinin/github-markdown-toc`
