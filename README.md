# BasicLibraryApp

Bu proje, temel bir kütüphane yönetim sistemi uygulamasıdır. Kitapların, kategorilerin ve okuyucuların yönetimini sağlayan bir .NET Core tabanlı web uygulamasıdır.

## 🚀 Özellikler

- Kitap yönetimi (ekleme, silme, güncelleme, listeleme)
- Kategori yönetimi
- Okuyucu yönetimi
- Kitap-okuyucu ilişkilendirme
- Kategori bazlı kitap filtreleme

## 🏗️ Proje Yapısı

Proje, N-Tier (Çok Katmanlı) mimari kullanılarak geliştirilmiştir:

- **Core**: Temel varlık sınıfları ve iş mantığı

  - Models: Book, Category, BookReader
  - DTOs: Veri transfer nesneleri
  - Services: İş mantığı arayüzleri
  - Repositories: Veri erişim arayüzleri
  - UnitOfWork: İşlem yönetimi

- **Repository**: Veritabanı işlemleri

  - Entity Framework Core implementasyonu
  - Veritabanı bağlantı yönetimi

- **Service**: İş mantığı katmanı

  - Core katmanındaki servis arayüzlerinin implementasyonu
  - İş kuralları ve validasyonlar

- **Linqq**: Kullanıcı arayüzü/API katmanı
  - Web API endpoints
  - Kullanıcı arayüzü

## 🛠️ Teknolojiler

- .NET Core
- Entity Framework Core
- SQL Server
- C#
- LINQ

## 📋 Gereksinimler

- .NET Core SDK 6.0 veya üzeri
- SQL Server
- Visual Studio 2022 veya Visual Studio Code

## 🔧 Kurulum

1. Projeyi klonlayın:

```bash
git clone https://github.com/yourusername/BasicLibraryApp.git
```

2. Proje dizinine gidin:

```bash
cd BasicLibraryApp
```

3. Veritabanı bağlantı dizesini `appsettings.json` dosyasında güncelleyin

4. Veritabanını oluşturun:

```bash
dotnet ef database update
```

5. Projeyi çalıştırın:

```bash
dotnet run
```

## 📚 Veri Modelleri

### Book (Kitap)

- Id: Benzersiz tanımlayıcı
- Title: Kitap başlığı
- Author: Yazar
- PublishDate: Yayın tarihi
- CategoryId: Kategori referansı
- Category: Kategori ilişkisi
- Readers: Okuyucu listesi

### Category (Kategori)

- Id: Benzersiz tanımlayıcı
- Name: Kategori adı
- Books: Kitap listesi

### BookReader (Okuyucu)

- Id: Benzersiz tanımlayıcı
- Name: Okuyucu adı
- Email: E-posta adresi
- ReadedBooks: Okunan kitaplar listesi

## 🤝 Katkıda Bulunma

1. Bu depoyu fork edin
2. Yeni bir özellik dalı oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some amazing feature'`)
4. Dalınıza push edin (`git push origin feature/amazing-feature`)
5. Bir Pull Request oluşturun

## 📝 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.
