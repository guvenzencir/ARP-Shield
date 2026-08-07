kkk# 🛡️ ARP-Shield: Active Firewall Defense
![Banner](https://via.placeholder.com/1200x300.png?text=ARP-Shield+Active+Defense)

ARP-Shield, ağ üzerindeki ARP Poisoning (Zehirlenmesi) saldırılarını tespit edip, saldırganı anında karantinaya alan Python ve Scapy tabanlı bir siber güvenlik aracıdır.

## 🚀 Özellikler
* **Sürekli Dinleme (Sniffing):** Ağdaki ARP Request ve Reply paketlerini arka planda pasif olarak analiz eder.
* **Anomali Tespiti:** Ağ geçidinin MAC adresiyle eşleşmeyen sahte paketleri anında yakalar.
* **Aktif İzolasyon (iptables):** Saldırganı tespit ettiği milisaniye içerisinde `iptables` üzerinden engelleyerek (DROP) ana sistemin internet bağlantısını kesintisiz korur.
* **Statik ARP Koruması:** Modemin MAC adresini işletim sisteminin ARP tablosunda statik olarak kilitleyerek zehirlenmeyi imkansız hale getirir.

## 🛠️ Gereksinimler
Projeyi çalıştırmak için sisteminizde Python 3 ve Scapy yüklü olmalıdır.

Kütüphaneyi kurmak için:
`pip install scapy`

## 💻 Kullanım
Güvenlik duvarı (`iptables`) ve statik ARP ataması gibi kernel seviyesinde işlemler yapıldığı için araç **root (sudo)** yetkileriyle çalıştırılmalıdır.

`sudo python3 arp_detector.py`

*Not: Script içerisindeki `GATEWAY_IP` ve `IFACE` değişkenlerini kendi ağ yapılandırmanıza göre düzenlemeyi unutmayın.*

## ⚠️ Yasal Uyarı ve Sorumluluk Reddi
Bu proje tamamen **eğitim, araştırma ve test amaçlı** geliştirilmiştir. 
Araç, yalnızca yetkiniz olan kendi yerel ağlarınızda (laboratuvar ortamlarında) savunma mekanizmalarını (Blue Team) anlamak ve test etmek için kullanılmalıdır. Bu aracın yetkisiz ağlarda veya kötü niyetli amaçlarla kullanılmasından doğacak her türlü yasal sorumluluk son kullanıcıya aittir. Geliştirici hiçbir sorumluluk kabul etmez.
