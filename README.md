# Mahalle Veri packages

Neighbourhood-level GeoPackage data with documented sources and dates. Load them into QGIS in
one click with the [Mahalle Veri plugin](https://github.com/CagriBurk/mahalle-veri-qgis), or
drag a `.gpkg` file into QGIS directly.

- **Packages:** on the [Releases](../../releases) page, one release per package
  (for example `izmir-2023-2026-11-19`).
- **Contents (İzmir):** neighbourhood boundaries with population, age, marital status,
  buildings, density, parks and amenity counts; district indicators from TÜİK; amenity,
  transit stop and park layers; a `metadata` table with the URL, licence and date of every
  source.
- Unknown values are left empty (NULL); `0` is used only when a value is known to be zero.
- **Licence:** ODbL 1.0 (derived from OpenStreetMap). Other sources: İzmir Metropolitan
  Municipality Open Data Portal (CC BY 4.0) and TÜİK.

---

## Türkçe

Mahalle düzeyinde, kaynağı ve tarihi belli veri paketleri (GeoPackage). Paketler QGIS'e [Mahalle Veri eklentisiyle](https://github.com/CagriBurk/mahalle-veri-qgis) tek tıkla yüklenir. Eklentisiz de açılabilir: bir `.gpkg` dosyasını QGIS'e sürükleyip bırakmanız yeterli.

- **Paketler:** [Releases](../../releases) sayfasında. Her paket ayrı bir sürümdür, örneğin `izmir-2023-2026-11-19`.
- **Katalog:** `katalog` sürümündeki `katalog.json` dosyası. Eklenti bu dosyayı okur; elle değiştirilmez.
- Paketler otomatik olarak üretilir ve buraya yüklenir.

## İçerik (İzmir)

| Katman | İçerik |
|---|---|
| `mahalle` | OSM mahalle sınırları. Her mahallede şu bilgiler var: nüfus (erkek, kadın, toplam, 0–14 yaş), medeni durum, bina sayıları, yoğunluk, parklar ve yeşil alan, donatı sayıları, toplu ulaşım durak sayıları |
| `ilce` | İlçe sınırları. Yaş grupları, hanehalkı göstergeleri ve TÜİK ilçe göstergeleri (nüfus, artış hızı, doğum, ölüm, evlenme, boşanma) |
| `donati`, `durak`, `park` | Eğitim, sağlık ve toplanma alanı noktaları; toplu ulaşım durakları; OSM parkları |
| `ilce_yas` | İlçe × yaş grubu × cinsiyet tablosu |
| `metadata` | Her kaynak için URL, lisans, kaynak gösterimi, yayın tarihi ve indirme tarihi |
| `paket_bilgisi` | Üretim tarihi, eşleşme oranı ve uyarılar (örneğin indirilemeyen kaynaklar) |

Değeri bilinmeyen alanlar **boş (NULL)** bırakılır. "0" yalnızca gerçekten sıfır olduğu bilinen değerler için kullanılır.

## Lisans ve kaynak gösterimi

Paketler OpenStreetMap verisinden türetilmiştir ve **Open Database License (ODbL) 1.0** ile lisanslanır: https://opendatacommons.org/licenses/odbl/1-0/

Kullanırken şu kaynak gösterimlerini ekleyin. Tam liste her paketin `metadata` tablosunda bulunur:
- © OpenStreetMap katkıcıları (ODbL)
- Kaynak: İzmir Büyükşehir Belediyesi Açık Veri Portalı (CC BY 4.0). Veri üreticisi: TÜİK.
- Kaynak: TÜİK
