# Gözde Plastik — Katalog Sitesi Kullanım Kılavuzu

Bu kılavuz teknik bilgi gerektirmez. Adım adım takip et.

---

## Yeni Ürün Nasıl Eklenir

1. Excel dosyasını aç (data/ klasöründe)
2. Son SKU'ya bak, bir sonrakini yaz (örn: FB-TOP-009)
3. Yeni satır aç, şu alanları doldur:
   - SKU, Ürün Adı, Kategori, Alt Tip, Ağırlık, Boyut
4. "Fotoğraf Dosya" sütununa: **SKU.jpg** yaz (örn: FB-TOP-009.jpg)
5. Excel'i kaydet
6. Terminal aç → `python scripts/excel_to_csv.py` yaz → Enter
7. Site güncellendi ✓

---

## Fotoğraf Nasıl Eklenir

1. Ürünü beyaz zemin üzerinde, doğal ışıkta çek
2. Dosyayı **SKU.jpg** olarak kaydet (örn: FB-TOP-001.jpg)
3. `public/images/` klasörüne koy
4. Bitti — site otomatik gösterir, başka işlem gerekmez ✓

---

## Site Nasıl Güncellenir

Excel değiştikten sonra:
```
python scripts/excel_to_csv.py
```
Sonra Netlify'a klasörü tekrar sürükle bırak.

---

## Netlify'a İlk Yükleme

1. [netlify.com](https://netlify.com) adresine git
2. Giriş yap (ücretsiz hesap aç)
3. "Add new site" → "Deploy manually" seç
4. `gozde-katalog-proje` klasörünü sürükle bırak
5. Birkaç saniye bekle — site linki hazır ✓

---

## Sorun Giderme

| Sorun | Çözüm |
|-------|-------|
| Site açılmıyor | CSV dosyası data/ klasöründe mi? |
| Fotoğraf görünmüyor | Dosya adı tam SKU.jpg mi? Büyük/küçük harf? |
| Türkçe karakter bozuk | Excel'i UTF-8 BOM olarak kaydet |
| Ürün listede çıkmıyor | "Aktif" sütunu "Evet" yazıyor mu? |

---

## İletişim & Destek

WhatsApp: 0532 415 76 11  
Adres: İstoç Toptancılar Çarşısı 18. Ada No:20-22, Bağcılar/İstanbul
