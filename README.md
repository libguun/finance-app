# 💰 Миний Санхүү — Cloudflare Pages

## Файлын бүтэц
```
finance-app/
├── public/
│   └── index.html          ← Апп (frontend)
├── functions/
│   └── api/
│       └── scan.js         ← Cloudflare Worker (backend)
└── README.md
```

## Cloudflare Pages дээр байршуулах алхмууд

### 1. GitHub repo үүсгэх
1. [github.com](https://github.com) → New repository
2. Нэр өгнө (жишээ: `my-finance-app`)
3. Энэ `finance-app` хавтасны бүх файлыг upload хийнэ

### 2. Cloudflare Pages холбох
1. [dash.cloudflare.com](https://dash.cloudflare.com) нэвтэрнэ
2. **Pages** → **Create a project** → **Connect to Git**
3. GitHub бүртгэлтэй холбоно
4. Repo сонгоно
5. Build settings:
   - **Framework preset:** None
   - **Build command:** (хоосон)
   - **Build output directory:** `public`
6. **Save and Deploy** дарна

### 3. API Key тохируулах ⚠️ ЧУХАЛ
1. Deploy дууссаны дараа **Settings** → **Environment variables**
2. **Add variable** дарна:
   - Variable name: `ANTHROPIC_API_KEY`
   - Value: `sk-ant-api03-xxxxxx` (таны жинхэнэ API key)
3. **Save** → **Redeploy**

### 4. Утсандаа суулгах
1. Cloudflare өгсөн линкийг (`xxx.pages.dev`) Safari-д нээнэ
2. Share → **Add to Home Screen**
3. Болоо! 🎉

## API Key авах
[console.anthropic.com](https://console.anthropic.com) → API Keys → Create Key
