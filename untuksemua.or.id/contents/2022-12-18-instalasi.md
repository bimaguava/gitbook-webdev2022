---
description: Proses instalasi dan build theme menggunakan NextJS
---

# 2022-12-18 Instalasi

## Prerequisite

Instalasi saya lakukan tanpa opsi `-g` kecuali `next`

* npm v9.2.0
* nodejs v18.12.1
* react
* react-dom
* next

## Build dan Testing

### Error Code ERESOLVE

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>npm install</p></figcaption></figure>

Bisa di `--force` sehingga, error tersebut dapat diminimalisir

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>npm install --force</p></figcaption></figure>

### Error Failed to load next.config.js

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>npm run dev</p></figcaption></figure>

Menandakan ada error di bundle-analyzer. Setelah baca di [sini](https://www.npmjs.com/package/@next/bundle-analyzer) :

> From version 2.0.0 of next-compose-plugins you need to call bundle-analyzer in this way to work

Dan setelah diteliti siapa yang salah, ternyata saat dicoba _run_ _locally_ ada error npm ERR! `Invalid comparator: npm:@keyvhq/core@~1.6.6`. Jadi, cobalah delete node, npm dan hapus node\_modules dan clear cache.

Lalu, renungi pesan dibawah ini

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>Deploy langsung di vercel</p></figcaption></figure>

## Edit sana-sini
