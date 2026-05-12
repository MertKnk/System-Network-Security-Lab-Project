# 🛡️ Domain Controller - Account Lockout Policy

Bu klasör, Active Directory ortamında kullanıcı hesaplarını Brute-Force (Kaba Kuvvet) saldırılarına karşı korumak için yapılandırdığım güvenlik politikalarını içerir.

## 🛠️ Uygulama Adımları

### 1. Politika Düzenleme (GPO Edit)
Yapılandırmaya başlamak için **Group Policy Management** konsolu üzerinden ilgili politika düzenleme moduna alınmıştır.
* **Path:** `Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy`

### 2. Kritik Güvenlik Ayarları
Ekran görüntülerinde detaylandırıldığı üzere şu kısıtlamalar uygulanmıştır:

* **Account lockout threshold (5 invalid logon attempts):** Kullanıcı 5 kez hatalı şifre girerse hesabı kilitlenir. Bu, saldırganın sınırsız deneme yapmasını engeller.
* **Account lockout duration (30 minutes):** Kilitlenen hesap 30 dakika boyunca kapalı kalır. Bu süre, otomatik saldırı araçlarını (botları) yavaşlatır ve etkisiz hale getirir.
* **Reset account lockout counter after (30 minutes):** Hatalı deneme sayacı her 30 dakikada bir sıfırlanır.

## 🚀 Teknik Kazanım
Bu hardening (sıkılaştırma) çalışmasıyla, domain ortamındaki kullanıcı hesaplarının ele geçirilme riskini minimize ettim ve saldırı maliyetini artırarak sistem güvenliğini üst seviyeye çıkardım.
