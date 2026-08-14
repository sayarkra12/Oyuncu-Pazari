# Görünüm ve Modeller

## Hologramlar

Kiralık, kiralanmış ve ürünü bekleyen pazarlar için ayrı hologram satırları tanımlanabilir. Kullanılabilen değerler:

| Değer | Açıklama |
|---|---|
| `%owner%` | Pazar sahibinin adı |
| `%item%` | Satıştaki ürünün adı |
| `%price%` | Ürünün satış fiyatı |
| `%time%` | Kalan kiralama süresi |
| `%rent_price%` | Pazar kiralama ücreti |
| `%market_id%` | Pazar kimliği |
| `%items%` | Aktif ürün sayısı |
| `%tax%` | Hesaplanan vergi |
| `%net%` | Vergi sonrası net kazanç |

`hologram.height` ve `hologram.line-spacing` ile konumlandırma yapılabilir. Desteklenen yeni sürümlerde billboard, hizalama, gölge ve arkasını gösterme seçenekleri de kullanılabilir.

Modern sürümlerde `TextDisplay` ve `ItemDisplay` kullanılır. Bu varlıkları desteklemeyen eski sürümlerde sistem otomatik olarak ArmorStand görünümüne geçer.

## Pazar modeli

Varsayılan görünüm Vanilla oyuncu kafasıdır. `display` bölümünden aşağıdaki yöntemlerden biri seçilebilir:

- Base64 özel kafa dokusu
- Vanilla materyal
- CustomModelData
- ItemsAdder öğesi
- Oraxen öğesi
- Nexo öğesi

Özel sağlayıcı kullanırken `display.provider` değerini `ITEMSADDER`, `ORAXEN` veya `NEXO` yapın. Kiralık ve kiralanmış durumlar için geçerli öğe kimliklerini girin. Sağlayıcı veya öğe bulunamazsa sistem Vanilla görünüme döner.

`display.vertical-offset`, görünür modelin kayıtlı pazar noktasına göre dikey konumunu düzenler.

Sonraki bölüm: [[Veri Güvenliği|Veri-Guvenligi]]
# Oyuncu Pazarı

> **Ücretli ve lisanslı ürün:** Bu wiki yalnızca dokümantasyondur. Kaynak kod, `.jar`, `.zip` veya eklenti indirme bağlantısı içermez. Satın alma, lisanslama ve dosya teslimi yalnızca resmi Discord sunucumuz üzerinden yapılır.

Oyuncu Pazarı; Minecraft sunucularında yöneticilerin fiziksel satış noktaları oluşturmasını, oyuncuların bu noktaları kiralamasını ve güvenli biçimde eşya alıp satmasını sağlayan bir pazar eklentisidir.

## Başlıca özellikler

- Yönetici tarafından istenen konuma yerleştirilen fiziksel pazar noktaları
- GUI üzerinden kiralama, ürün ekleme, satın alma, süre uzatma ve kapatma
- Oyuncu başına izin tabanlı kiralama limitleri
- Ayarlanabilir süre, fiyat, vergi ve güvenlik seçenekleri
- SQLite tabanlı kalıcı pazar, ürün, teslimat ve kazanç verileri
- Para/eşya kaybını önlemeye yönelik işlem ve kurtarma sistemi
- Modern sürümlerde `TextDisplay`/`ItemDisplay`, eski sürümlerde ArmorStand görünümü
- Vanilla, özel kafa, CustomModelData, ItemsAdder, Oraxen ve Nexo model desteği
- Spigot, Paper ve Folia uyumluluğu
- Sunucu/IP tabanlı çevrim içi lisans doğrulaması

## Kitap bölümleri

1. [[Satın Alma ve Lisans|Satin-Alma-ve-Lisans]]
2. [[Kurulum|Kurulum]]
3. [[Hızlı Başlangıç|Hizli-Baslangic]]
4. [[Komutlar ve Yetkiler|Komutlar-ve-Yetkiler]]
5. [[Yapılandırma|Yapilandirma]]
6. [[Görünüm ve Modeller|Gorunum-ve-Modeller]]
7. [[Veri Güvenliği|Veri-Guvenligi]]
8. [[Sorun Giderme|Sorun-Giderme]]

## Gereksinimler

| Bileşen | Durum | Açıklama |
|---|---|---|
| Minecraft sunucu yazılımı | Gerekli | Spigot, Paper veya Folia; API hedefi 1.16 ve üzeridir. |
| Java | Gerekli | En az Java 16. Sunucu sürümünüz daha yeni Java isteyebilir. |
| Vault | Gerekli | Para çekme ve yatırma işlemleri için kullanılır. |
| Ekonomi eklentisi | Gerekli | Vault ile çalışan bir ekonomi sağlayıcısı kurulmalıdır. |
| İnternet bağlantısı | Gerekli | Lisans doğrulama servisine erişilebilmelidir. |
| ItemsAdder / Oraxen / Nexo | İsteğe bağlı | Özel pazar modeli kullanılacaksa yalnızca seçilen sağlayıcı gerekir. |

## Destek

Satın alma, güncelleme, lisans taşıma ve teknik destek işlemleri resmi Discord sunucumuz üzerinden yürütülür. Destek talebinde sunucu sürümünü, Java sürümünü ve ilgili konsol hata mesajını belirtin. Lisans veya özel erişim bilgilerini herkese açık kanallarda paylaşmayın.

---

**GitHub sayfası yalnızca bilgi amaçlıdır; eklenti dosyası buradan indirilemez.**
