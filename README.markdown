# NMAP (Network Mapper)

## بسم الله الرحمن الرحيم

Waxaad igal soo xiriiri kartaa:

- Phone: +252 619987794
- Telegram: [https://t.me/hacking_akhlaaqyin](https://t.me/hacking_akhlaaqyin)
- TikTok: [https://www.tiktok.com/@arkani657](https://www.tiktok.com/@arkani657)

---

## 1. HORDHAC

### Waa Maxay Nmap?
Nmap, oo sidoo kale loo yaqaan Network Mapper, waa a (open-source tool) oo awood leh oo loo isticmaalo baaritaanka shabakadaha (network scanning) waa sida khariidad(mapper) oo ogaanaya qaab-dhismeedka shabakadda, (live hosts), ports-yada furan (open ports), iyo adeegyada (services) ka socda bartilmaameedka. Waxaa markii ugu horreysay soo saaray Gordon Lyon (oo loo yaqaan "Fyodor") sanadkii 1997, isagoo ku daabacay majaladda Phrack Magazine. Tan iyo markaas, Nmap wuxuu noqday mid ka mid ah qalabka ugu muhiimsan ee loo isticmaalo (network security) iyo ethical hacking-ga—waa aalad lagu kalsoonaan karo oo loogu talagalay in lagu ogaado meelaha shabakadda iyo in lagu wanaajiyo ammaankeeda.

Nmap wuxuu awood u leeyahay inuu baaro shabakadaha waaweyn iyo kuwa yaryar—laga bilaabo shabakadda gurigaaga ilaa shabakadaha shirkadaha waaweyn. Waa qalab loogu talagalay inuu caawiyo dadka doonaya inay bartaan sida shabakadaha u shaqeeyaan, sida loo ogaado daciifnimada (vulnerabilities), iyo sida loo ilaaliyo nidaamyada.

### Sida ay u Bilowday
Gordon Lyon wuxuu sameeyey Nmap si uu u fududeeyo baaritaanka shabakadaha—markii hore wuxuu ahaa qalab fudud oo loogu talagalay baaritaanka ports-yada, laakiin sannadihii la soo dhaafay, wuxuu noqday aalad badan oo leh sifooyin badan oo loo isticmaali karo ujeedooyin kala duwan.

---

## 2. MUHIIMADDA NMAP

### Muxuu Nmap Muhiim u Yahay?
Nmap aad ayuu muhiim u yahay sababtoo ah wuxuu bixiyaa awoodo kala duwan oo lagu baaro, lagu falanqeeyo, waa qalab loo isticmaalo in lagu caawiyo ogaanshaha daciifnimada, kuwaan waa sababaha ugu waaweyn ee Nmap muhiim u tahay, oo aan si qoto dheer uga hadli doono mid kasta:

- **Baadhitaanka Shabakadaha si loo Ogaado Ports Furan iyo Adeegyada Shaqaynaya**  
  Nmap wuxuu ogaadaa ports-yada furan (open ports)—kuwaas oo ah ports (host)—iyo adeegyada ka socda, waxaad ogaan kartaa in port 80 uu furan yahay oo Apache HTTP server uu ku shaqaynayo.  
  *Tusaale*: Markaad qorto `nmap 192.168.1.100` Kali VM-kaaga oo aad ogaato `80/tcp open http`, waxaad ogaanaysaa in adeeg HTTP uu shaqaynayo.

- **Tijaabinta Amniga si loo Aqoonsado Meelaha Daciifka ah**  
  Nmap wuxuu caawiyaa ogaanshaha meelaha daciifka ah (vulnerabilities) ee shabakadda, haddii port 445 uu furan yahay oo Samba duug ah uu shaqaynayo, waxay noqon kartaa daciifnimo laga faa'iideysan karo.  
  *Tusaale*: Markaad isticmaasho `nmap -sV 192.168.1.100` oo aad ogaato `445/tcp open smb Samba 3.0.20`, waxaad ogaan kartaa in version-kan uu leeyahay daciifnimo la ogyahay (CVE-2017-7494).

- **Maareynta Shabakadaha**  
  Nmap wuxuu ogaanayaa (active hosts) ee shabakadda.  
  *Tusaale*: Markaad qorto `nmap -sn 192.168.1.0/24` oo aad ogaato `192.168.1.100 wuu shaqeynaa`, waxaad ogaanaysaa active hosts.

---

## 3. ASTAAMAHA MUHIIMKA AH EE NMAP

Nmap wuxuu leeyahay sifooyin badan oo awood leh oo ka dhigaya qalab badan (versatile)—halkan waxaa ah sifooyinka ugu muhiimsan ee Nmap, oo aan si qoto dheer uga hadli doono mid kasta si aad u fahanto sida ay u shaqeeyaan iyo sababta ay muhiim u yihiin:

- **Ncrack – Baaritaanka (Password Testing)**  
  *Waa Maxay*: Ncrack waa qalab ka mid ah qoyska Nmap oo loo isticmaalo (password cracking) waxaad tijaabin kartaa password-ka SSH.  
  *Sida ay u Shaqeyso*: Ncrack wuxuu isku dayayaa ereyada sirta ah ee caadiga ah (bruteforce) ama liisaska sirta si uu u ogaado kuwa daciifka ah, waxaad isticmaali kartaa `ncrack -p ssh 192.168.1.100` si aad u tijaabiso SSH login.  
  *Tusaale*: Markaad qorto `ncrack -p ssh -U usernames.txt -P passwords.txt 192.168.1.100` (halkan usernames.txt iyo passwords.txt waa faylal aad abuurtay oo leh liisaska username iyo password-kooda), waxaad ogaan kartaa password SSH ee bartilmaameedka.

- **Ncat – Xiriir Ammaan ah iyo Gudbinta Xogta**  
  *Waa Maxay*: Ncat waa qalab ka mid ah Nmap oo loo isticmaalo samaynta isku-xirnaansho shabakadeed (connections) iyo gudbinta xogta—waa sida Netcat, laakiin leh sifooyin dheeraad ah sida (encryption). Waxaad abuuri kartaa xiriir ammaan leh u dhexeeya Kali VM-kaaga iyo Metasploitable VM-kaaga.  
  *Sida ay u Shaqeyso*: Ncat wuxuu dhegeystaa (listens) ama ku xiraa (connects) ports-yada.  
  *Tusaale*: Markaad qorto `ncat -l 4444` terminal hal ka mid ah Kali VM-kaaga oo aad qorto `ncat 127.0.0.1 4444` terminal kale, waxaad samayn doontaa xiriir TCP—markaad qorto "Salaan" terminal-ka client-ka, waxaad arki doontaa "Salaan" oo ka soo muuqda terminal-ka listener-ka.

- **Nping – Tijaabinta Isku-xirka Shabakadda**  
  *Waa Maxay*: Nping waa qalab ka mid ah Nmap oo loo isticmaalo tijaabinta isku-xirka shabakadda (network connectivity)—waa qalab loogu talagalay in lagu ogaado sida shabakaddu ugu jawaabto baakadaha xogta (packets).  
  *Sida ay u Shaqeyso*: Nping wuxuu soo diraa baakadaha ICMP, TCP, ama UDP si uu u arko jawaabaha.  
  *Tusaale*: Markaad qorto `nping -c 10 192.168.1.100` Kali VM-kaaga, waxaad arki doontaa "10 packets sent, 10 packets received, 0% packet loss"—tani waxay muujinaysaa in bartilmaameedka ("target") shaqaynayo oo jawaabaya.

- **Zenmap – Interface (GUI)**  
  *Waa Maxay*: Zenmap waa interface garaafixi ah (Graphical User Interface - GUI) ee Nmap—waa qayb ka mid ah Nmap oo loo isticmaalo in lagu fududeeyo baaritaanka shabakadda.  
  *Sida ay u Shaqeyso*: Zenmap wuxuu kuu ogolaanayaa inaad geliso IP-ga bartilmaameedka oo aad doorato nooca baaritaanka (tusaale, Quick Scan, Intense Scan).  
  *Tusaale*: Markaad furto Zenmap qor "scanme.nmap.org" goobta "Target", doorato "Intense Scan", oo gujiso "Scan", waxaad arki doontaa natiijooyin sida "22/tcp open ssh, 80/tcp open http" qaab fudud oo garaafixi ah.

- **Nmap Scripting Engine (NSE) – Automation iyo Raadinta Daciifnimada**  
  *Waa Maxay*: Nmap Scripting Engine (NSE) waa qayb ka mid ah Nmap oo loo isticmaalo automation (isku-dubbaridinta hawlaha) iyo raadinta daciifnimada (vulnerability detection)—wuxuu ogolaanaya inaad isticmaasho scripts si aad u ogaato daciifnimada iyo xog dheeraad ah.  
  *Sida ay u Shaqeyso*: NSE wuxuu leeyahay scripts badan oo hore loo sameeyay.  
  *Tusaale*: Markaad qorto `nmap --script http-enum 192.168.1.100` Kali VM-kaaga, waxaad ogaan kartaa directories qarsoon ee Apache ee Metasploitable VM—tusaale, "/admin" ama "/phpmyadmin".

---

## 4. WAXYAABAHA SAAMEYN KARA NATIIJOOYINKA NMAP SCAN

Intaadan isticmaalin Nmap, waa muhiim inaad fahanto waxyaabaha saameyn kara natiijooyinka baaritaanka—halkan waxaa ah sharraxaad faahfaahsan oo ku saabsan arrimaha saameynaya iyo sida loo maareeyo si aad u hesho natiijooyin sax ah.

- **Firewalls, Routers, iyo Proxy Servers**  
  Firewalls, routers, iyo proxy servers waa nidaamyada amniga ee shabakadda oo xannibi kara ama qarin kara xogta la helayo—tusaale, firewall wuxuu xannibi karaa ports-yada si aadan u arkin natiijooyin sax ah.  
  *Saameynta*: Haddii firewall uu xannibo port 80 Nmap wuxuu sheegi doonaa "filtered" halkii "open" laga sheegi lahaa—tani waxay ka dhigan tahay in natiijooyinkaagu aysan noqon karin kuwo sax ah.  
  *Tusaale*: Markaad qorto `nmap 192.168.1.100` oo aad aragto `80/tcp filtered`, waxay ka dhigan tahay in firewall uu xannibay.

- **Root Privileges**  
  *Waa Maxay*: Haddii aad baarayso qalab fog (remote host) ka baxsan VM-kaaga gaarka ah, waxaad u baahan kartaa (root privileges) si aad u hesho natiijooyin sax ah.  
  *Saameynta*: Haddii aadan isticmaalin root privileges, Nmap waxaa laga yaabaa inuusan baarin dhammaan ports-yada ama uusan helin jawaabo sax ah.

- **Baaritaanka aan Fasax lahayn**  
  Baaritaanka shabakadaha bilaa oggolaansho wuxuu keeni karaa dhibaatooyin.  
  Haddii aad baarto shabakad aan laguu oggolayn, ISP-gaaga wuxuu ku soo diri karaa digniin, ama booliisku ayaa ku xiri doona, laakin wax xog ah kama hayo in Soomaali arintaa darteed laguu xiri karo, laakin ALLAH ka cabsada shabakad aan laguu ogoleyn scan ha marinin.

---

## 5. DIGNIINO MUHIIM AH

Nmap waa qalab awood leh, laakiin waa in si taxaddar leh loo isticmaalo—halkan waxaa ah digniino faahfaahsan oo muhiim ah oo aad fahanto si aad u isticmaasho Nmap.

- **Ha Baarin Shabakado aan Fasax Lagaa Siinin!**  
  Kor ayaan ugu soo hadalnay.

- **Si xoog scan ha u marin**  
  Baaritaanka (aggressive scans) sida `nmap -A` ama baaritaanka ports-yada badan si dhakhso ah wuxuu dhaawici karaa nidaamyada daciifka ah.  
  *Tusaale*: Haddii aad qorto `nmap -A -T5 192.168.1.100` (T5 waa xawaaraha ugu sarreeya) laga yaabaa inuu dhaacow software duug ah ama daciif ah.  
  *Sida loo Ilaaliyo*: Isticmaal baaritaanka caadiga ah (default settings) ama xawaaraha dhexe (tusaale, -T3).

---

## 6. SIDA LOO RAKIBO NMAP

### Rakibidda Windows
1. Booqo websaydka rasmiga ah: [https://nmap.org/download.html](https://nmap.org/download.html)
2. Soo dejiso installer-ka Windows
3. Riix installer-ka oo raac tilmaamaha  
   Nmap wuxuu u baahan yahay WinPCap/Npcap si uu u qabto xirmada xogta

### Rakibidda Linux
Waxaad isticmaali kartaa (package manager) si aad u rakibto Nmap:
- Ubuntu/Debian:  
  ```
  sudo apt update
  sudo apt install nmap
  ```
- Fedora/RHEL:  
  ```
  sudo dnf install nmap
  ```
- Arch Linux:  
  ```
  sudo pacman -S nmap
  ```

### Rakibidda (Source)
```
wget https://nmap.org/dist/nmap-VERSION.tar.bz2
tar xjf nmap-VERSION.tar.bz2
cd nmap-VERSION
./configure
make
sudo make install
```

### Rakibidda MacOS
- Isticmaal Homebrew:  
  ```
  brew install nmap
  ```
- Ama soo dejiso installer-ka MacOS ka websaydka rasmiga ah

---

## 7. WAA MAXAY NMAP SCRIPTING ENGINE (NSE)?

Nmap Scripting Engine (NSE) wuxuu ka mid yahay Nmap oo loo isticmaalo automation (isku-dubbaridinta hawlaha) iyo raadinta daciifnimada (vulnerability detection)—waa qayb awood leh oo Nmap oo kuu ogolaanaysa inaad isticmaasho scripts hore loo sameeyad ama aad abuurto scripts gaar ah si aad u ogaato daciifnimada, xog dheeraad ah, ama u tijaabiso adeegyada.

### Sida loo Isticmaalo NSE
- Isticmaalka Scripts-ka Caadiga ah: `nmap -sC [bartilmaameed]`  
  *Tusaale*: `nmap -sC 192.168.1.100`
- Isticmaalka Script Gaar ah: `nmap --script=[scriptname] [bartilmaameed]`  
  *Tusaale*: `nmap --script=http-enum 192.168.1.100`
- Isticmaalka Scripts-ka Qaybta: `nmap --script=[category][bartilmaameed]`  
  *Tusaale*: `nmap --script=vuln 192.168.1.100`

### Qaybaha Scripts-ka NSE
- auth: Scripts-ka la xiriira xaqiijinta
- broadcast: Scripts-ka ogaanshaha broadcast
- brute: Scripts-ka weerarrada brute force
- default: Scripts-ka caadiga ah ee la isticmaalo -sC
- discovery: Scripts-ka ogaanshaha hosts iyo adeegyada
- dos: Scripts-ka Denial of Service
- exploit: Scripts-ka ka faa’ideysiga “markaad ogaato meesha ka jilcan bartilmaameedka oo aad ka faa’ideysaneyso”
- vuln: Scripts-ka ogaanshaha daciifnimada

---

## 8. SCRIPTS-YADA MUHIIMKA AH EE NSE

Nmap Scripting Engine (NSE) waxay leedahay scripts badan oo waxtar leh—halkan waxaa ah sharraxaad faahfaahsan oo ku saabsan scripts-ka ugu waxtarka badan ee aad isticmaali karto si aad u ogaato shabakadda lab-yada waxbarashada si sharci ah—oo leh tusaalooyin:

- **http-enum**  
  *Waa Maxay*: http-enum waa script NSE oo loo isticmaalo in lagu ogaado directories iyo files caadiga ah ee servers-ka web-ka—waa qalab loogu talagalay in lagu ogaado meelaha daciifka ah ee servers-ka web-ka—tusaale, waxaad ogaan kartaa in server-ka web-ku leeyahay directory "/admin" oo aan la ilaalin.  
  *Sida loo Isticmaalo*: `nmap --script=httpenum [bartilmaameed]`  
  *Tusaale*: `nmap --script=http-enum 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu kaa caawinayaa inaad ogaato meelaha daciifka ah ee servers-ka web-ka, sida directories aan la ilaalin ama files muhiim ah oo si fudud loo heli karo.

- **smb-vuln-ms17-010**  
  *Waa Maxay*: smb-vuln-ms17-010 waa script NSE oo loo isticmaalo in lagu ogaado daciifnimada EternalBlue (MS17-010) ee adeegyada SMB—waa qalab loogu talagalay in lagu ogaado haddii server-ku yahay mid daciif u ah weerarka EternalBlue.  
  *Sida loo Isticmaalo*: `nmap --script=smb-vuln-ms17-010 [bartilmaameed]`  
  *Tusaale*: `nmap --script=smb-vuln-ms17-010 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu kaa caawinayaa inaad ogaato haddii server-ku yahay mid daciif u ah weerarka EternalBlue, taas oo keeni karta in la qabsado server-ka.

- **ssl-heartbleed**  
  *Waa Maxay*: ssl-heartbleed waa script NSE oo loo isticmaalo in lagu ogaado daciifnimada Heartbleed ee adeegyada SSL/TLS—waa qalab loogu talagalay in lagu ogaado haddii server-ku yahay mid daciif u ah weerarka Heartbleed.  
  *Sida loo Isticmaalo*: `nmap --script=ssl-heartbleed [bartilmaameed]`  
  *Tusaale*: `nmap --script=ssl-heartbleed 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu kaa caawinayaa inaad ogaato haddii server-ku yahay mid daciif u ah weerarka Heartbleed, taas oo keeni karta in la xado xogta muhiimka ah sida furaha sirta ah.

- **ftp-anon**  
  *Waa Maxay*: ftp-anon waa script NSE oo loo isticmaalo in lagu ogaado haddii server-ka FTP-gu ogolaado gelitaanka anonymous—waa qalab loogu talagalay in lagu ogaado haddii server-ka FTP-ku yahay mid aan la ilaalin.  
  *Sida loo Isticmaalo*: `nmap --script=ftp-anon [bartilmaameed]`  
  *Tusaale*: `nmap --script=ftp-anon 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu kaa caawinayaa inaad ogaato haddii server-ka FTP-ku ogolaado gelitaanka anonymous, taas oo keeni karta in la helo files muhiim ah oo aan la ilaalin.

- **http-sql-injection**  
  *Waa Maxay*: http-sql-injection waa script NSE oo loo isticmaalo in lagu ogaado daciifnimada SQL injection ee applications-ka web-ka—waa qalab loogu talagalay in lagu ogaado haddii application-ka web-ku yahay mid daciif u ah weerarka SQL injection.  
  *Sida loo Isticmaalo*: `nmap --script=http-sql-injection [bartilmaameed]`  
  *Tusaale*: `nmap --script=http-sql-injection 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu kaa caawinayaa inaad ogaato haddii application-ka web-ku yahay mid daciif u ah weerarka SQL injection, taas oo keeni karta in la helo xogta muhiimka ah ee database-ka.

---

## 9. SIDA LOO HELO SCRIPTS-YADA NSE

Helitaanka scripts-ka NSE waa habka lagu ogaado, lagu cusbooneysiiyo, ama looga beddelo scripts-yada Nmap Scripting Engine—waa qalab loogu talagalay in lagu helo scripts-yada hore loo sameeyad.

### Sida loo Arko Scripts-yada la Heli karo
- **Liiska Scripts-yada Ku Rakiban**:  
  ```
  ls /usr/share/nmap/scripts/
  ```
  *Tusaale*: `ls /usr/share/nmap/scripts/ | grep http`
- **Raadinta Scripts-yada**:  
  ```
  grep -l "description" /usr/share/nmap/scripts/*.nse
  ```
  *Tusaale*: `grep -l "SQL injection" /usr/share/nmap/scripts/*.nse`
- **Cusbooneysiinta Scripts-yada**:  
  ```
  nmap --script-updatedb
  ```

---

## 10. AMARRO AASAASIGA AH EE NMAP

### Baaritaanka Aasaasiga ah
- **Baaritaanka Host Keliya**:  
  ```
  nmap [bartilmaameed]
  ```
  *Tusaale*: `nmap 192.168.1.100`
- **Baaritaanka Shabakad**:  
  ```
  nmap [network/CIDR]
  ```
  *Tusaale*: `nmap 192.168.1.0/24`

### Baaritaanka Ports-yada
- **Baaritaanka Port Gaar ah**:  
  ```
  nmap -p [port] [bartilmaameed]
  ```
  *Tusaale*: `nmap -p 80 192.168.1.100`
- **Baaritaanka Ports Badan**:  
  ```
  nmap -p [port1,port2,port3] [bartilmaameed]
  ```
  *Tusaale*: `nmap -p 22,80,443 192.168.1.100`
- **Baaritaanka Dhammaan Ports-yada**:  
  ```
  nmap -p- [bartilmaameed]
  ```
  *Tusaale*: `nmap -p- 192.168.1.100`

### Baaritaanka Adeegyada
- **Ogaanshaha Adeegyada**:  
  ```
  nmap -sV [bartilmaameed]
  ```
  *Tusaale*: `nmap -sV 192.168.1.100`
- **Ogaanshaha Adeegyada oo Faahfaahsan**:  
  ```
  nmap -sV --version-intensity [1-9] [bartilmaameed]
  ```
  *Tusaale*: `nmap -sV --version-intensity 7 192.168.1.100`

### Baaritaanka Nidaamka OS
- **Ogaanshaha Nidaamka**:  
  ```
  nmap -O [bartilmaameed]
  ```
  *Tusaale*: `nmap -O 192.168.1.100`
- **Baaritaan Dhammaystiran**:  
  ```
  nmap -A [bartilmaameed]
  ```
  *Tusaale*: `nmap -A 192.168.1.100`

---

## 11. NOOCYADA BAARITAANKA (SCAN TYPES)

- **TCP SYN Scan (Stealth Scan)**  
  TCP SYN scan waa nooca baaritaanka caadiga ah ee Nmap—waxaa loo yaqaan "half-open" scan sababtoo ah ma dhammaystirto handshake TCP—waa qalab loogu talagalay in lagu ogaado ports-yada furan si qarsoon.  
  *Sida loo Isticmaalo*: `nmap -sS [bartilmaameed]`  
  *Tusaale*: `nmap -sS 192.168.1.100`  
  *Faa'iidooyinka*: Waa mid ka qarsoon baaritaanka TCP connect, waa mid ka dhakhso badan baaritaanka TCP connect.  
  *Cillad*: Waxay u baahan tahay root/administrator privileges.

- **TCP Connect Scan**  
  TCP connect scan waa nooca baaritaan marka aadan lahayn root/administrator privileges—wuxuu dhammaystiraa TCP handshake oo dhan—waa qalab loogu talagalay in lagu ogaado ports-yada furan.  
  *Sida loo Isticmaalo*: `nmap -sT [bartilmaameed]`  
  *Tusaale*: `nmap -sT 192.168.1.100`  
  *Faa'iidooyinka*: Ma u baahna root/administrator privileges, waa mid ka sax badan baaritaanka SYN.  
  *Cillad*: Waa mid cad baaritaankiisa SYN oo waxaa fudud in lagu ogaado, waa mid ka gaabiya baaritaanka SYN.

- **UDP Scan**  
  UDP scan waa nooca baaritaanka Nmap ee loo isticmaalo in lagu ogaado ports-yada UDP ee furan—waa qalab loogu talagalay in lagu ogaado adeegyada UDP sida DNS, SNMP, iyo DHCP.  
  *Sida loo Isticmaalo*: `nmap -sU [bartilmaameed]`  
  *Tusaale*: `nmap -sU 192.168.1.100`  
  *Faa'iidooyinka*: Wuxuu baaraa adeegyada UDP ee inta badan la ilaawaa, wuxuu ogaadaa adeegyada muhiimka ah sida DNS iyo DHCP.

- **FIN, NULL, iyo XMAS Scans**  
  *Waa Maxay*: FIN, NULL, iyo XMAS scans waa noocyada baaritaanka ee Nmap ee loo isticmaalo in lagu ogaado ports-yada furan si qarsoon—waa qalab loogu talagalay in lagu dhaafi karo firewalls-ka qaarkood.  
  *Sida loo Isticmaalo*:  
  ```
  nmap -sF [bartilmaameed]  # FIN scan
  nmap -sN [bartilmaameed]  # NULL scan
  nmap -sX [bartilmaameed]  # XMAS scan
  ```
  *Tusaale*: `nmap -sF 192.168.1.100`  
  *Faa'iidooyinka*: Waa kuwo ka qarsoon baaritaanka SYN mararka qaarkood, waxay dhaafi karaan firewalls-ka qaarkood.  
  *Cillad*: Kuma shaqeeyaan Windows-ka, waa kuwo aan la hubin sida SYN scan.

---

## 12. TUSAALOOYIN MUHIIM AH

### Tusaalooyin Aasaasiga ah
- **Baaritaanka Aasaasiga ah**: `nmap 192.168.1.100`  
  *Natiijooyinka*: Wuxuu muujinayaa ports-yada caadiga ah ee furan.
- **Baaritaanka Shabakad oo Dhan**: `nmap 192.168.1.0/24`  
  *Natiijooyinka*: Wuxuu muujinayaa dhammaan hosts-ka shaqeynaya iyo ports-yada furan.
- **Baaritaanka Adeegyada**: `nmap -sV 192.168.1.100`  
  *Natiijooyinka*: Wuxuu muujinayaa adeegyada iyo versions-kooda.

### Tusaalooyin wanaagsan
- **Baaritaan Dhammaystiran**: `nmap -A -T4 192.168.1.100`  
  *Natiijooyinka*: Wuxuu muujinayaa ports-yada, adeegyada, versions-ka, nidaamka, iyo macluumaad dheeraad ah.
- **Baaritaanka Daciifnimada**: `nmap --script=vuln 192.168.1.100`  
  *Natiijooyinka*: Wuxuu muujinayaa daciifnimada la ogyahay ee bartilmaameedka.
- **Baaritaanka Qarsoon**: `nmap -sS -T2 192.168.1.100`  
  *Natiijooyinka*: Wuxuu muujinayaa ports-yada furan si qarsoon.

---

## 13. SOURCES

### Websaydyo
- [Nmap.org](https://nmap.org) - Websaydka rasmiga ah ee Nmap
- [Nmap Documentation](https://nmap.org/book/) - Buugga rasmiga ah ee Nmap
- [HackerTarget Nmap Tutorial](https://hackertarget.com/nmap-tutorial/)