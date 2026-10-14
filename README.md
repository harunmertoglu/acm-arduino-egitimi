# ACM Arduino Eğitimi — Buzzer ile Şarkılar

Arduino Uno ve pasif buzzerlarla melodi çalmak için hazırlanmış 30 örnek kod.
Her şarkının **tek, iki ve beş buzzer** için ayrı sürümü bulunur.

## Hangi klasörü seçmeliyim?

| Buzzer sayısı | Kodlar | Artı (+) uçların bağlanacağı pinler |
|---|---|---|
| 1 | [1_Buzzer](1_Buzzer) | D7 |
| 2 | [2_Buzzer](2_Buzzer) | D7 ve D8 |
| 5 | [5_Buzzer](5_Buzzer) | D4, D5, D6, D7 ve D8 |

Her buzzerın eksi (−) ucu **GND** pinine bağlanır. Bağlantı değişikliklerini
kartın enerjisini keserek yapın. Arduino çıkış pinlerini birbirine bağlamayın.
Kodlar pasif buzzer içindir. Doğrudan pin bağlantısı uygun düşük akımlı piezo
buzzerlarda kullanılmalıdır; daha yüksek akımlı parçalar için uygun sürücü gerekir.

## Başlamak için

1. Bu sayfada **Code → Download ZIP** ile dosyaları indirin ve ZIP'i açın.
2. Buzzer sayınıza uygun klasöre girin, `00_ONCE_OKU.txt` rehberini okuyun.
3. Arduino IDE'de yeni bir proje açın.
4. İstediğiniz şarkının `.txt` dosyasının **tamamını** editöre yapıştırın.
   Dosya başındaki açıklamalar kod yorumudur; silmeniz gerekmez.
5. Kart olarak **Arduino Uno**, port olarak bağlı Uno'nun portunu seçin.
6. **Yükle** düğmesine basın. Şarkı otomatik başlar ve bekleyerek tekrar eder.

Her dosya bağımsız bir programdır. Aynı projeye birden fazla şarkı dosyasını
birleştirmeyin. `BPM` değerini artırmak hızlandırır, azaltmak yavaşlatır;
BPM ses yüksekliği ayarı değildir.

## Şarkılar

Her üç klasörde de aşağıdaki dosyalar vardır:

| Dosya | İçerik |
|---|---|
| `01_Zamansizlik.txt` | Manifest — Zamansızlık |
| `02_Hileli.txt` | Manifest x Ajda Pekkan — Hileli |
| `03_Cav_Bella.txt` | Çav Bella |
| `04_Bir_Derdim_Var_Tam.txt` | Mor ve Ötesi — Bir Derdim Var, tam bölüm |
| `05_Bir_Derdim_Var_Nakarat.txt` | Bir Derdim Var, yalnızca nakarat |
| `06_Tame_Impala_Piyano_Bolumu.txt` | Tame Impala, paylaşılan 16 ölçülük piyano bölümü |
| `07_Adi_Belirtilmeyen_Sarki_Iki_Versiyon.txt` | Yazılı notasyondan aktarılan, iki versiyonlu parça |
| `08_Adi_Belirtilmeyen_Sarki_Gorsel.txt` | Numaralı nota görselinden aktarılan parça |
| `09_Ariyo.txt` | Manifest — Arıyo |
| `10_Aya_Benzer.txt` | Mustafa Sandal — Aya Benzer |

07 numaralı dosyada `VERSIYON` sabitini `1` veya `2` yaparak seçim yapılır.
07 ve 08 numaralı parçaların adı belirtilmediği için genel adlar kullanılmıştır.

### Tame Impala düzenlemesi

- Tek buzzer: D7 ana melodiyi çalar; bas ve akorun diğer sesleri çıkarılmıştır.
- İki buzzer: D7 ana melodiyi, D8 bası çalar.
- Beş buzzer: D4–D6 melodi ve akorları, D7–D8 bası çalar.

Diğer şarkılarda tüm bağlı buzzerlar aynı melodiyi birlikte çalar.

## Kontrol ve kapsam

30 kodun tamamı Arduino CLI ile `arduino:avr:uno` hedefi için derlenmiştir.
Bu kontrol derlenebilirliği gösterir; gerçek donanımda ses, bağlantı ve nota
doğruluğu için dinleme testi yapılmamıştır. Ritimler yaklaşık uyarlamalardır;
bu dosyalar profesyonel nota edisyonu değildir.

İlk paylaşılan nota görsellerindeki kaynak: [kolaynota.com](https://www.kolaynota.com/).
Şarkı adları ve sanatçı bilgileri ilgili dosyaların başında belirtilmiştir.
