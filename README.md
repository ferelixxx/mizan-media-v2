# Mizân — Gönül Sesleri Ses Arşivi

Bu depo, [Mizân](https://mizanguide.com) uygulamasının **"Gönül Sesleri"** bölümü için üretilen anlatım ses dosyalarını barındırır. Uygulama bu dosyaları `raw.githubusercontent.com` üzerinden doğrudan çeker; referanslar uygulamanın Firestore veritabanında tutulur.

## Anlatıcı

Tüm parçalar, uygulamanın sabit rehber karakteri tarafından okunur:

- 🇹🇷 **Hızır**
- 🇬🇧 **Al-Khidir**
- 🇸🇦 **الخضر**

Sesler Google Cloud (Gemini-TTS) ile üretilmiştir.

## Yapı

180 dosya, 4 kategori × 15 konu × 3 dil (`tr` / `en` / `ar`) olacak şekilde düzenlenmiştir:

| Klasör | Kategori | Konu sayısı | Dosya sayısı |
|---|---|---|---|
| `peygamberlerin_izinde/` | Peygamberlerin İzinde | 15 | 45 |
| `kuran_kissalari/` | Kur'an Kıssaları | 15 | 45 |
| `kuranda_kavramlar/` | Kur'an'da Kavramlar | 15 | 45 |
| `sahabe_portreleri/` | Sahabe Portreleri | 15 | 45 |

### Dosya adlandırma

```
<konu_slug>_<dil>.mp3
```

Örnek: `hz_yusuf_tr.mp3`, `hz_yusuf_en.mp3`, `hz_yusuf_ar.mp3`

Tüm dosya adları küçük harf, alt çizgi ile ayrılmış, saf ASCII karakterlerden oluşur (Türkçe özel karakter veya boşluk içermez) — bu, ham (`raw`) bağlantıların hiçbir URL kodlaması gerektirmeden doğrudan çalışmasını sağlar.

### Kapak görselleri

`covers/` klasörü, her konu için **tek bir** kapak görseli barındırır (3 dil ortak kullanır). Adlandırma: `<konu_slug>.webp` — örn. `hz_adem.webp`. Ayrıntı için [`covers/README.md`](covers/README.md).

## Kullanım

Uygulama, Firestore'daki her ses kaydının bağlantısını şu formatta bekler:

```
https://raw.githubusercontent.com/ferelixxx/mizan-media-v2/main/<klasör>/<dosya_adı>
```

## Telif Hakkı

© Mizân. Tüm hakları saklıdır. Bu ses kayıtları yalnızca Mizân uygulaması içinde kullanılmak üzere üretilmiştir; üçüncü taraflarca yeniden dağıtılamaz, ticari amaçla kullanılamaz veya türev içerik üretiminde kaynak olarak alınamaz.
