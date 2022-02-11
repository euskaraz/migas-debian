# migas-debian

<h3>Debian edo behin-behineko zerbitzarian kudeatuko diren ordenagailuetan instalatzeko paketeak.</h3>


1. Sistemaren arkitektura egiaztatu:
    <code># uname -r</code>
    
2. Repositorio honetatik DEB paketeak deskargatu.
ADI!!: aurreko pausuaren arabera aukeratu dagokion migasfree-play_1.5.0.1_xxx.deb paketea

3. Instalatu paketeak:

    <code>    dpkg -i migasfree-client_4.18-1_all.deb </code>

    Arkitekturaren arabera 386 edo amd64 paketea instalatu.
    
    <code>    dpkg -i migasfree-play_1.5.0.1_xxx.deb </code>

    <code>    dpkg -i aek89*.deb </code>
    
    
4. Aurreko pausuan menpekotasunengatiko errorea gerta daiteke. Horrela gertatzekotan egin:

    <code> # apt -f install </code>
    
    eta beharrezko pakete guztiak instalatuko dira.
 
5. Migasfree automatiko abiatu ahal izateko WAYLAND desgaitu.

    <code> # nano /etc/gdm3/daemon.conf </code>
    WAYLAND ENABLE=FALSE lerroa deskomentatu

6. Erabiltzaile zerrenda desgaitu saioa hasteko pantailan.

    <code> # nano /etc/gdm3/greeter.dconf-defaults</code>
    #- disable-user-list=true lerroa deskomentatu
    
