# PHP Format tanggal bahasa indonesia
[![StyleCI](https://github.styleci.io/repos/201660628/shield?branch=master)](https://github.styleci.io/repos/201660628)
[![Build Status](https://travis-ci.org/nim4n136/format-tanggal-indonesia.svg?branch=master)](https://travis-ci.org/nim4n136/format-tanggal-indonesia)
 [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
 


Untuk mempermudah membuat format tanggal pada php dalam bahasa indonesia, seperti menampilkan nama hari, menampilkan nama bulan, tahun, jam, dll

### Instalasi menggunakan composer
```
composer require nim4n/simple-date-format
```
### Penggunaan

##### Contoh sederhana
```php

include './vendor/autoload.php';
use Nim4n\SimpleDate;

$contohFormatTanggal = "2019-08-16 23:21";

echo SimpleDate::date($contohFormatTanggal); // Output: 16 Agustus 2019
echo SimpleDate::dayDate($contohFormatTanggal); // Output: Jumat, 16 Agustus 2019

// dengan menggunakan jam dan menit
echo SimpleDate::dateTime($contohFormatTanggal); // Output: 16 Agustus 2019 00:00
echo SimpleDate::dayDateTime($contohFormatTanggal); // Output: Jumat, 16 Agustus 2019 00:00

// dengan nama bulan di singkat
echo SimpleDate::shortMonthDate($contohFormatTanggal); // 16 Agt 2019
// dengan nama bulan di singkat tambah waktu jam menit
echo SimpleDate::shortMonthDateTime($contohFormatTanggal); // 16 Agt 2019 23:21

// dengan nama hari dan nama bulan di singkat
echo SimpleDate::dayShortMonthDate($contohFormatTanggal); //Jumat, 16 Agt 2019 
// dengan nama hari dan nama bulan di singkat tambah jam waktu
echo SimpleDate::dayShortMonthDateTime($contohFormatTanggal); //Jumat, 16 Agt 2019 23:21

// hanya tanggal dan bulan
echo SimpleDate::onlyDateMonth($contohFormatTanggal);
// hanya tanggal dan bulan di singkat
echo SimpleDate::onlyDateShortMonth($contohFormatTanggal);

// hanya tahun
echo SimpleDate::onlyYear($contohFormatTanggal); // 2019
// hanya hari
echo SimpleDate::onlyDay($contohFormatTanggal); // Jumat
// hanya bulan
echo SimpleDate::onlyMonth($contohFormatTanggal); // Agustus
// hanya jam
echo SimpleDate::onlyHour24($contohFormatTanggal); // 23
// Hanya menit
echo SimpleDate::onlyMinute($contohFormatTanggal); // 21

```
