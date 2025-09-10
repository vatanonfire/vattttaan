# Fal Platform

Modern fal baktırma ve ritüel platformu. El falı, yüz falı, kahve falı ve AI destekli yorumlar sunan web uygulaması.

## Özellikler

- 🔐 Kullanıcı kayıt ve giriş sistemi
- 👤 Profil yönetimi
- 🪙 Koin sistemi
- 📱 Responsive tasarım
- 🎨 Modern UI/UX
- 🔒 Güvenli API
- 📊 Admin paneli

## Teknolojiler

### Frontend
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- Framer Motion
- React Hot Toast
- Lucide React Icons

### Backend
- Node.js
- Express.js
- TypeScript
- Prisma ORM
- PostgreSQL
- JWT Authentication
- bcryptjs

## Kurulum

### Gereksinimler
- Node.js 18+
- PostgreSQL
- npm veya yarn

### 1. Repository'yi klonlayın
```bash
git clone <repository-url>
cd fal
```

### 2. Backend kurulumu
```bash
cd backend
npm install
```

### 3. Veritabanı kurulumu
```bash
# .env dosyasını oluşturun
cp env.example .env

# Veritabanı URL'sini güncelleyin
# DATABASE_URL="postgresql://username:password@localhost:5432/fal_platform"

# Prisma migration'ları çalıştırın
npx prisma migrate dev

# Seed data (opsiyonel)
npx prisma db seed
```

### 4. Backend'i başlatın
```bash
npm run dev
# http://localhost:5000
```

### 5. Frontend kurulumu
```bash
cd ../frontend
npm install
```

### 6. Frontend'i başlatın
```bash
npm run dev
# http://localhost:3000
```

### 7. Kolay Başlatma (Windows)
```bash
# PowerShell ile (önerilen)
.\start-system.ps1

# Veya Batch dosyası ile
start-system.bat
```

### 8. Servisleri Durdurma
```bash
# PowerShell ile
.\stop-system.ps1

# Veya Batch dosyası ile
stop-system.bat
```

### 9. Production Deployment
```bash
# Netlify için frontend build
cd frontend && npm run build

# Backend için production build
cd backend && npm run build
```

**Not**: Production deployment için Netlify ve Heroku kullanılabilir. Detaylar için `NETLIFY_DEPLOYMENT.md` dosyasına bakın.

## Script'ler

### Ana Script'ler
```bash
npm run dev              # Backend ve frontend'i aynı anda başlatır
npm run build            # Backend ve frontend'i build eder
npm run install:all      # Tüm bağımlılıkları kurar
npm run setup            # Tam kurulum (bağımlılıklar + veritabanı)
```

### Ayrı Script'ler
```bash
npm run dev:backend      # Sadece backend'i başlatır
npm run dev:frontend     # Sadece frontend'i başlatır
npm run build:backend    # Sadece backend'i build eder
npm run build:frontend   # Sadece frontend'i build eder
```

## Kullanım

### Kullanıcı İşlemleri
1. **Kayıt Ol**: `/auth/register` sayfasından yeni hesap oluşturun
2. **Giriş Yap**: `/auth/login` sayfasından giriş yapın
3. **Profil**: `/profile` sayfasından bilgilerinizi düzenleyin

### Fal İşlemleri
- El falı, yüz falı, kahve falı seçenekleri
- Günlük 3 ücretsiz fal hakkı
- AI destekli yorumlar
- Koin ile ek fal hakkı satın alma

### Admin Panel
- Kullanıcı yönetimi
- Fal istatistikleri
- Sistem ayarları

## API Endpoints

### Auth
- `POST /api/auth/register` - Kullanıcı kaydı
- `POST /api/auth/login` - Kullanıcı girişi
- `GET /api/auth/me` - Mevcut kullanıcı bilgileri
- `POST /api/auth/logout` - Çıkış

### User
- `PUT /api/user/profile` - Profil güncelleme

### Fortune
- `POST /api/fortune/hand` - El falı
- `POST /api/fortune/face` - Yüz falı
- `POST /api/fortune/coffee` - Kahve falı

## Ortam Değişkenleri

### Backend (.env)
```env
DATABASE_URL="postgresql://username:password@localhost:5432/fal_platform"
JWT_SECRET="your-secret-key"
CORS_ORIGIN="http://localhost:3000"
PORT=5000
NODE_ENV=development
```

## Geliştirme

### Veritabanı şemasını güncelleme
```bash
cd backend
npx prisma migrate dev --name migration_name
```

### Production build
```bash
# Backend
cd backend
npm run build
npm start

# Frontend
cd frontend
npm run build
npm start
```

## Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit yapın (`git commit -m 'Add amazing feature'`)
4. Push yapın (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## İletişim

Proje Sahibi - [@your-username](https://github.com/your-username)

Proje Linki: [https://github.com/your-username/fal-platform](https://github.com/your-username/fal-platform)
