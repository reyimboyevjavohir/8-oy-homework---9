# PsixoHelp v3 — Ishga tushirish

## Talablar
- Node.js 18+
- PostgreSQL

## 1. PostgreSQL baza yaratish
```bash
sudo -u postgres psql
```
```sql
CREATE DATABASE psixologik_db;
\q
```

## 2. Backend sozlash
```bash
cd apps/backend
cp .env.example .env
```

`.env` faylni oching va to'ldiring:
```env
DATABASE_URL="postgresql://postgres:PAROLINGIZ@localhost:5432/psixologik_db"
JWT_SECRET="o'zingiz-biladigan-maxfiy-kalit"
GROQ_API_KEY="gsk_..."   # https://console.groq.com dan oling
```

```bash
npm install
npx prisma migrate deploy
npx prisma generate
npm run dev
```

## 3. Frontend sozlash
```bash
cd apps/frontend
npm install --legacy-peer-deps
npm run dev
```

## Manzillar
- Frontend: http://localhost:3000
- Backend:  http://localhost:4000
- Health:   http://localhost:4000/api/health
# 8-oy-homework---9
# 8-oy-homework---9
