# Ali Rıza Birdal — Portföy

Tek dosyalık statik site. Derleme yok, bağımlılık yok.

## GitHub Pages'te yayınlamak

1. GitHub'da yeni bir repo aç: **`alirizabirdal.github.io`**
   (kullanıcı adın neyse `KULLANICIADI.github.io` — bu isim önemli, kök adres verir)
2. Bu klasördeki her şeyi repoya yükle (`index.html`, `img/`, `README.md`).
   - Web'den: repo sayfasında **Add file → Upload files** → klasörü sürükle → Commit
   - Terminalden:
     ```
     git init
     git add .
     git commit -m "portfolio"
     git branch -M main
     git remote add origin https://github.com/KULLANICIADI/KULLANICIADI.github.io.git
     git push -u origin main
     ```
3. Repo → **Settings → Pages** → Source: `Deploy from a branch`, Branch: `main` / `root` → Save
4. 1-2 dakika sonra `https://KULLANICIADI.github.io` adresinde yayında.

> Repo adını `portfolio` gibi başka bir şey yaparsan adres
> `https://KULLANICIADI.github.io/portfolio/` olur — o da çalışır.

## Kendi domainini bağlamak

Domain aldıysan (örn. `alirizabirdal.com`):
1. Settings → Pages → **Custom domain** kutusuna yaz, Save
2. Domain sağlayıcında DNS kaydı ekle:
   - `A` kaydı → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - veya `CNAME` (www için) → `KULLANICIADI.github.io`
3. **Enforce HTTPS** kutusunu işaretle

## İş eklemek

`index.html` içinde en alttaki `ISLER` listesini düzenle. Yorum satırındaki
şablonları kopyala, `/* */` işaretlerini sil, doldur.

```js
{kat:"3d", en:6, img:"img/3d/zuber-01.jpg", marka:"Züber", yil:"2025",
 baslik:"Ürün gamı 3D modelleme",
 problem:"Tek satır: hangi problem vardı?",
 cozum:"Tek satır: nasıl çözdün?",
 vaka:{brief:"...", surec:["adım","adım"], sonuc:"..."}}
```

- `kat`: `motion` · `3d` · `sosyal` · `web` — filtre butonları otomatik oluşur
- `en`: kart genişliği — `4` dar, `6` yarım, `12` tam genişlik
- `yt`: YouTube video ID (`youtu.be/ABC123` → `ABC123`). Üstüne gelince sessiz oynar.
- `img`: görsel yolu. Görsel bulunamazsa site bozulmaz, uyarı gösterir.
- `vaka`: yazarsan kartta **VAKA →** butonu çıkar, yandan panel açılır. Yazmazsan çıkmaz.

## Görseller

`img/sosyal/`, `img/motion/`, `img/web/`, `img/3d/` klasörlerine at.
Kare/dikey işler için `en:4`, geniş işler için `en:6` veya `12` kullan.
Dosyaları 1600px genişliği geçmeyecek şekilde ve JPG olarak kaydet (site hızlı kalsın).
