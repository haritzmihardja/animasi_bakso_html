# Deskripsi Teknis File Blender: Animasi Iklan Bakso Realistis

---

## 1. Struktur Scene

- **Collection:**
  - `Gerobak_Bakso`: Model gerobak, posisi di (0, 0, -3)
  - `Abang_Bakso`: Karakter manusia (Mixamo/Sketchfab), posisi di belakang gerobak
  - `Mangkuk`: Model mangkuk, posisi di atas meja depan abang
  - `Bakso`: 3–5 buah, masuk ke mangkuk satu per satu
  - `Mie`, `Tahu`, `Sayur`: Diletakkan di mangkuk
  - `Kuah`: Mesh tipis, texture permukaan minyak
  - `Topping`: Bawang goreng, seledri, sambal, dsb (particle/mesh kecil di atas bakso)
  - `Meja`: Box, posisi di depan gerobak
  - `Kamera`: Animasi sesuai storyboard

---

## 2. Lighting

- **HDRI:** Night street (download dari [Poly Haven](https://polyhaven.com/hdris))
- **Lampu tambahan:** Area light di atas mangkuk untuk highlight bakso

---

## 3. Kamera & Animasi

- **Kamera utama:**
  - Frame 1–60: Kamera mendekat ke gerobak (opening)
  - Frame 61–120: Kamera ke abang bakso
  - Frame 121–250: Kamera ke mangkuk, close-up saat penyajian
  - Frame 251–350: Kamera zoom in ke bakso, efek depth of field
  - Frame 351–450: Kamera ke logo/teks closing
- **Animasi tangan abang bakso:**
  - Ambil mangkuk, ambil bakso, menuang kuah (bisa pakai rig Mixamo atau keyframe sederhana)
- **Animasi bakso:**
  - Bakso masuk ke mangkuk satu per satu (frame 130, 150, 170, dst)
- **Animasi kuah:**
  - Kuah muncul setelah bakso masuk (frame 200)
- **Efek steam:**
  - Particle system/smoke di atas mangkuk (start frame 210)

---

## 4. Material & Texture

- **Bakso:**
  - Material Principled BSDF
  - Color: tekstur dari foto bakso asli (bump/normal map untuk urat)
  - Roughness: 0.21, Clearcoat: 0.3, Subsurface: 0.18
- **Kuah:**
  - Texture permukaan minyak (bisa dari foto kuah bakso)
  - Transparan, sedikit glossy
- **Mangkuk, Gerobak, Topping:**
  - Material dan texture sesuai referensi video

---

## 5. Setting Render

- **Engine:** Cycles (untuk realisme maksimal)
- **Resolution:** 1920x1080 (Full HD)
- **Frame Rate:** 30 fps
- **Output:** .mp4 (FFmpeg video), encoding H.264
- **Sampling:** 128–512 (tinggi = lebih halus)
- **Motion Blur:** ON
- **Depth of Field:** ON (kamera close-up bakso)

---

## 6. Cara Penggunaan

1. **Import semua model 3D** ke Blender, sesuaikan posisi sesuai struktur di atas.
2. **Apply texture/material** pada bakso, kuah, mangkuk, gerobak, dsb.
3. **Setup HDRI** untuk lighting malam hari.
4. **Atur kamera & animasi** sesuai urutan frame di atas.
5. **Tambahkan efek steam** dengan particle system.
6. **Set output render** ke .mp4 (Output Properties > Output > File Format: FFmpeg Video, Encoding: MPEG4/H.264)
7. **Klik Render > Render Animation**.
8. **File video siap upload ke medsos.**

---

## 7. Saran Asset Gratis/Marketplace
- [Bakso 3D Model (Sketchfab)](https://sketchfab.com/search?q=bakso&type=models)
- [Gerobak Makanan (Sketchfab)](https://sketchfab.com/search?q=food+cart&type=models)
- [Mangkuk, Sendok, Topping (CGTrader)](https://www.cgtrader.com/3d-models/food/kitchenware/bowl-and-spoon)
- [Karakter Manusia (Mixamo)](https://www.mixamo.com/)
- [HDRI Night Street (Poly Haven)](https://polyhaven.com/hdris)

---

Jika ingin file .blend siap pakai, cukup serahkan dokumen ini ke animator Blender profesional atau freelancer, atau buat sendiri dengan mengikuti instruksi di atas.

**Selamat berkarya dan semoga sukses dengan iklan baksonya!**
