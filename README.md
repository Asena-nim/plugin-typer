# Typer for Photopea

Türkçe arayüzlü, manga/manhwa metinlerini stillerle Photopea'ya yerleştirmeye yardımcı olan eklenti.

## GitHub Pages

`main` dalı ve `/(root)` klasörü için GitHub Pages'i etkinleştirin. Yayın adresi:

`https://asena-nim.github.io/plugin-typer/`

## Photopea'da kullanma

1. GitHub repo'sunda **Settings → Pages** bölümünü açın.
2. **Deploy from a branch** seçin.
3. Branch olarak `main`, klasör olarak `/(root)` seçip **Save** tıklayın.
4. GitHub Pages dağıtımının tamamlanmasını bekleyin.
5. Photopea'yı açın ve **Window → Plugins** bölümünden eklenti ekleme/yönetme seçeneğini açın.
6. İstenirse şu URL'yi girin: `https://asena-nim.github.io/plugin-typer/plugin.html`
7. Photopea yalnızca klasör/manifest URL'si kabul ederse `https://asena-nim.github.io/plugin-typer/` adresini deneyin.

Photopea sürümüne göre menü adı değişebilir. URL ekleme seçeneği yoksa `plugin.html` dosyasını HTTPS üzerinden yayınlayan bir adres gerekir; `file://` adresiyle eklenti çalışmaz.

## Kullanım

- Metin alanına scripti yapıştırın.
- Bir satıra dokunarak seçin.
- Stil kartından font, boyut, önek, metin rengi ve kontur rengini seçin.
- **Sırayla Tek Tek Yerleştir** ile sırayla ilerleyin.
- **Toplu Metin Yerleşimi** için satır seçimlerini yapıp önizlemeyi onaylayın.
- Seçim alanı varsa metin alanın merkezine, yoksa belgenin merkezine yerleştirilir.
- Fontun Photopea oturumunda bulunması gerekir; eklentideki liste fontu yüklemez.

## Logo ve desen

Logo/desen dosyaları tarayıcı IndexedDB'sinde geçici olarak tutulur. Varsayılan saklama süresi 2 gündür. Bu kayıtlar cihaz ve tarayıcıya özeldir; düzenli olarak ayar JSON'u dışa aktarılmalıdır.

JPEG, PNG ve WebP desteklenir. PDF dosyaları listelenebilir ancak PDF'nin Photopea'ya katman olarak aktarılması tarayıcı/Photopea desteğine bağlıdır.

## Bilinen sınırlamalar

- Eklenti Photopea'nın sistem font listesini doğrudan okuyamaz.
- Eklenti Photopea'ya font kuramaz; fontu Photopea'ya ayrıca yüklemek gerekir.
- Yerel dosya verileri doğrudan JSX içine `File` olarak verilemez. Logo/desen aktarımı için Photopea'nın desteklediği dosya aktarım akışı kullanılmalıdır; Data URL'nin `new File(dataUrl)` ile açılması güvenilir değildir.
- Gelişmiş warp, dalga, gerçek clipping mask, gölge ve degrade işlemleri Photopea Action Manager komutlarıyla ayrıca doğrulanmalıdır.

## Geri dönüş

Bir sorun olursa GitHub commit geçmişinden önceki çalışan commit'e dönülebilir. Ayarları değiştirmeden önce eklenti içindeki JSON dışa aktarma özelliğini kullanın.
