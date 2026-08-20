# 🛡️ ARP-Shield: Active Firewall Defense

![Banner](https://via.placeholder.com/1200x300.png?text=ARP-Shield+Active+Defense)

🌍 **[Türkçe versiyonu için aşağıya kaydırın / Scroll down for Turkish](#-türkçe-sürüm)**

ARP-Shield is a Python and Scapy-based cybersecurity tool that detects ARP Poisoning attacks on the network and immediately quarantines the attacker.

## 🚀 Features

* **Continuous Sniffing:** Passively analyzes ARP Request and Reply packets on the network in the background.
* **Anomaly Detection:** Instantly catches forged packets that do not match the legitimate gateway's MAC address.
* **Active Isolation (iptables):** Blocks (DROP) the attacker via `iptables` within milliseconds of detection, ensuring uninterrupted internet connectivity for the host system.
* **Static ARP Protection:** Statically locks the router's MAC address in the operating system's ARP table, rendering poisoning attempts ineffective.

## 🛠️ Requirements

To run this project, you need to have Python 3 and Scapy installed on your system.

You can install the required library using pip:
```bash
pip install scapy
```

## 💻 Usage

Since the tool performs kernel-level operations such as firewall (`iptables`) modifications and static ARP assignments, it must be executed with **root (sudo)** privileges.

```bash
sudo python3 arp_detector.py
```

> **Note:** Do not forget to edit the `GATEWAY_IP` and `IFACE` variables inside the script to match your own network configuration.

---

# 🇹🇷 Türkçe Sürüm

ARP-Shield, ağ üzerindeki ARP Poisoning (Zehirlenmesi) saldırılarını tespit edip, saldırganı anında karantinaya alan Python ve Scapy tabanlı bir siber güvenlik aracıdır.

## 🚀 Özellikler

* **Sürekli Dinleme (Sniffing):** Ağdaki ARP Request ve Reply paketlerini arka planda pasif olarak analiz eder.
* **Anomali Tespiti:** Ağ geçidinin MAC adresiyle eşleşmeyen sahte paketleri anında yakalar.
* **Aktif İzolasyon (iptables):** Saldırganı tespit ettiği milisaniye içerisinde `iptables` üzerinden engelleyerek (DROP) ana sistemin internet bağlantısını kesintisiz korur.
* **Statik ARP Koruması:** Modemin MAC adresini işletim sisteminin ARP tablosunda statik olarak kilitleyerek zehirlenmeyi imkansız hale getirir.

## 🛠️ Gereksinimler

Projeyi çalıştırmak için sisteminizde Python 3 ve Scapy yüklü olmalıdır.

Kütüphaneyi kurmak için aşağıdaki komutu kullanabilirsiniz:
```bash
pip install scapy
```

## 💻 Kullanım

Güvenlik duvarı (`iptables`) yapılandırması ve statik ARP ataması gibi kernel seviyesinde işlemler yapıldığı için araç **root (sudo)** yetkileriyle çalıştırılmalıdır.

```bash
sudo python3 arp_detector.py
```

> **Not:** Script içerisindeki `GATEWAY_IP` ve `IFACE` değişkenlerini kendi ağ yapılandırmanıza göre düzenlemeyi unutmayın.

## ⚠️ Yasal Uyarı ve Sorumluluk Reddi
Bu proje tamamen **eğitim, araştırma ve test amaçlı** geliştirilmiştir. 
Araç, yalnızca yetkiniz olan kendi yerel ağlarınızda (laboratuvar ortamlarında) savunma mekanizmalarını (Blue Team) anlamak ve test etmek için kullanılmalıdır. Bu aracın yetkisiz ağlarda veya kötü niyetli amaçlarla kullanılmasından doğacak her türlü yasal sorumluluk son kullanıcıya aittir. Geliştirici hiçbir sorumluluk kabul etmez.
