# 🛡️ ARP-Shield: Moving Target Defense (MTD)
![Banner](https://via.placeholder.com/1200x300.png?text=ARP-Shield+Active+Defense)

ARP-Shield, ağ üzerindeki ARP Poisoning (Zehirlenmesi) saldırılarını tespit edip anında aktif savunma manevrası gerçekleştiren, Python ve Scapy tabanlı bir siber güvenlik aracıdır.

## 🚀 Özellikler
* **Sürekli Dinleme (Sniffing):** Ağdaki ARP Request ve Reply paketlerini arka planda pasif olarak analiz eder.
* **Anomali Tespiti:** Ağ geçidinin MAC adresiyle eşleşmeyen sahte paketleri anında yakalar.
* **Hareketli Hedef Savunması (MTD):** Saldırı tespit edildiği milisaniye içerisinde ağ arayüzünü izole eder.
* **Dinamik MAC Rotasyonu:** Sisteme rastgele ve temiz bir MAC adresi atayarak saldırganın hedefini tamamen boşa düşürür.

## 🛠️ Gereksinimler
Projeyi çalıştırmak için sisteminizde Python 3 ve Scapy yüklü olmalıdır.

Kütüphaneyi kurmak için:
`pip install scapy`

## 💻 Kullanım
Ağ arayüzlerine doğrudan müdahale ve paket dinleme işlemleri yapıldığı için araç **root (sudo)** yetkileriyle çalıştırılmalıdır.

`sudo python3 arp_detector.py`

*Not: Script içerisindeki `GATEWAY_IP` ve `IFACE` değişkenlerini kendi ağ yapılandırmanıza göre düzenlemeyi unutmayın.*

## ⚠️ Yasal Uyarı
Bu araç tamamen eğitim ve savunma amaçlı (Blue Team) geliştirilmiştir. Yalnızca yetkiniz olan ağlarda ve sistemlerde test ediniz.
