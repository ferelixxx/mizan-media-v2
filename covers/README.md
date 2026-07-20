# Kapak Görselleri

Her konunun **tek bir kapak görseli** olur; bu görsel o konunun 3 dildeki (tr/en/ar) ses parçası tarafından ortak kullanılır.

## Adlandırma

```
<konu_slug>.webp
```

Örnek: `hz_adem.webp`, `ashabi_kehf.webp`, `islamda_aile.webp`

`<konu_slug>`, ilgili ses dosyalarıyla aynı öneki paylaşır (`hz_adem_tr.mp3` / `hz_adem_en.mp3` / `hz_adem_ar.mp3` → kapak: `hz_adem.webp`).

Kategoriye göre alt klasör yok — 60 konunun tamamı tekil (benzersiz) slug'a sahip olduğundan tek düz klasör yeterli ve daha kolay yönetilir.

## Durum

Bu klasör şu an bir yer tutucudur. Gerçek görseller eklendikçe buraya `<konu_slug>.webp` adıyla yüklenmelidir; Firestore'daki `imageUrl` alanları bu isimlendirmeye göre önceden ayarlanmıştır.
