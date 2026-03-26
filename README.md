# YADA Dergisi — Etik Değerlendirme Modülü

## Klasör Yapısı
```
yada-app/
├── api/
│   └── evaluate.js     ← Güvenli API proxy (anahtar burada)
├── public/
│   └── index.html      ← Arayüz
├── vercel.json         ← Vercel ayarları
└── README.md
```

---

## Kurulum (5 adım)

### 1. GitHub'a Yükle
- github.com → "New repository" → `yada-app` adını ver
- Bu klasörün tüm içeriğini yükle

### 2. Vercel'e Bağla
- vercel.com → "Add New Project"
- GitHub reposunu seç → "Deploy" tıkla

### 3. API Anahtarını Gizlice Ekle
- Vercel Dashboard → projeniz → **Settings → Environment Variables**
- Name: `ANTHROPIC_API_KEY`
- Value: `sk-ant-api03-...` (anahtarınız)
- "Save" → **Redeploy**

### 4. URL'yi Al
- Vercel size `https://yada-app.vercel.app` gibi bir URL verir

### 5. k12.tr Sitesine Göm
Yönetici panelinde HTML/içerik kutusuna şunu ekleyin:

```html
<iframe 
  src="https://yada-app.vercel.app" 
  width="100%" 
  height="900" 
  style="border:none;border-radius:8px;"
  title="YADA Dergisi Makale Değerlendirme">
</iframe>
```

---

## Güvenlik
- API anahtarı hiçbir zaman tarayıcıda görünmez
- Tüm istekler sunucu üzerinden geçer
- Vercel Environment Variables şifreli saklanır
