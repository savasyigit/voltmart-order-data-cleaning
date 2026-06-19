# Voltmart Demand Forecasting Data Preparation

## English

### Project Overview

This project focuses on cleaning and preparing e-commerce order data for a Machine Learning team that plans to build a demand forecasting model.

Using PySpark, raw order data stored in a Parquet file is transformed into a clean and standardized dataset ready for analysis and modeling.

### Data Cleaning Tasks

The following transformations were applied:

- Removed orders placed between 12:00 AM and 5:59 AM.
- Removed all products containing the term "TV".
- Converted product names to lowercase.
- Converted category names to lowercase.
- Created a new `time_of_day` column:
  - `morning` → 05:00 - 11:59
  - `afternoon` → 12:00 - 17:59
  - `evening` → 18:00 - 23:59
- Extracted the state information from the purchase address.
- Converted the `order_date` column from timestamp to date format.
- Selected only the required columns for the final dataset.
- Saved the cleaned dataset in Parquet format.

### Technologies Used

- Python
- PySpark
- Apache Spark
- Parquet

### Input Dataset

```text
orders_data.parquet
```

### Output Dataset

```text
orders_data_clean.parquet
```

### Business Objective

The goal of this project is to provide a clean and reliable dataset that can be used to build demand forecasting models and support data-driven business decisions.

---

## Türkçe

### Proje Hakkında

Bu proje, talep tahminleme (Demand Forecasting) modeli geliştirecek olan Makine Öğrenmesi ekibi için e-ticaret sipariş verilerinin temizlenmesi ve hazırlanması amacıyla geliştirilmiştir.

Parquet formatında saklanan ham sipariş verileri, PySpark kullanılarak temizlenmiş, dönüştürülmüş ve analiz ile modelleme süreçlerinde kullanılabilecek standart bir yapıya getirilmiştir.

### Uygulanan Veri Temizleme İşlemleri

Aşağıdaki dönüşümler gerçekleştirilmiştir:

- Gece 00:00 ile sabah 05:59 arasında oluşturulan siparişler kaldırıldı.
- Ürün adında "TV" geçen kayıtlar veri setinden çıkarıldı.
- Ürün isimleri küçük harfe dönüştürüldü.
- Kategori isimleri küçük harfe dönüştürüldü.
- Sipariş saatine göre yeni bir `time_of_day` sütunu oluşturuldu:
  - `morning` → 05:00 - 11:59
  - `afternoon` → 12:00 - 17:59
  - `evening` → 18:00 - 23:59
- Adres bilgisinden eyalet bilgisi ayrıştırıldı.
- `order_date` sütunu tarih formatına dönüştürüldü.
- Nihai veri seti için gerekli sütunlar seçildi.
- Temizlenmiş veri Parquet formatında kaydedildi.

### Kullanılan Teknolojiler

- Python
- PySpark
- Apache Spark
- Parquet

### Girdi Veri Seti

```text
orders_data.parquet
```

### Çıktı Veri Seti

```text
orders_data_clean.parquet
```

### Projenin Amacı

Bu projenin amacı, makine öğrenmesi modellerinde kullanılabilecek kaliteli ve güvenilir bir veri seti oluşturarak talep tahminleme çalışmalarını desteklemektir.
