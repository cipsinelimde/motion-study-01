# MOTION / STUDY 01 — 10s

Tek dosyalık (`index.html`), **kodla üretilmiş 10 saniyelik motion design** parçası.
Kinetik tipografi + geometrik form + ışık süpürmesi; baştan sona kusursuz döngü
(seamless loop) olarak çalışır.

## Ne var?

- **Sahne 1 — MOTION (0.5–3.9 s):** harf harf yukarıdan gelen, 3D perspektifle
  dönen kinetik tipografi. `easeOutExpo` girişi, stagger'lı zamanlama.
- **Sahne 2 — Form (3.0–4.5 s):** halka, kare, üçgen ve parlayan nokta
  merkezde birleşir; ardından kelimeye yer açmak için dört yana açılır.
- **Sahne 3 — DESIGN (4.45–7.4 s):** gradyanlı kelime, geometriyle poster
  kompozisyonu kurar; nokta önde yörüngede döner.
- **Sahne 4 — End card (7.5–10 s):** çizilerek oluşan "M" markası, `10 SEC`,
  ince kural çizgisi ve künye.
- **HUD:** gerçek zamanlı zaman kodu, ilerleme çubuğu, tick cetveli, sweep motifi.

Tüm animasyon `requestAnimationFrame` üzerinde çalışan tek bir timeline
motoruyla sürülür; CSS keyframe bağımlılığı yoktur. Kare hızından bağımsız,
tıklayınca duraklatılabilir (`Space` de çalışır), `prefers-reduced-motion`
desteklenir.

## Çalıştırma

Tek dosya olduğu için doğrudan tarayıcıda açılabilir:

```bash
xdg-open index.html      # veya: python3 -m http.server 8000
```

Yayın adresi: <https://cipsinelimde.github.io/motion-study-01/>

## Zaman çizelgesi

| s | olay |
|---|------|
| 0.0 – 0.5 | boşluk, ışık süpürmesi, grid belirir |
| 0.55 – 2.9 | **MOTION** harfleri stagger'lı giriş |
| 2.95 – 3.95 | MOTION yukarı doğru bulanık çıkış |
| 3.05 – 3.8 | geometri merkezde toplanır |
| 3.82 – 4.77 | geometri kelimeye yer açmak için açılır |
| 4.45 – 6.8 | **DESIGN** harfleri giriş |
| 6.55 – 7.4 | DESIGN ölçeklenerek çıkış |
| 7.45 – 9.4 | end card kurulur (marka çizimi → 10 → kural → künye) |
| 9.6 – 10.0 | yumuşak karartma, döngü başı |

## Yapı

```
index.html    # tüm parça: işaretleme, stil, timeline motoru
favicon.svg   # gradyan "M" ikonu
poster.png    # 1920×1080 paylaşım görseli
```
