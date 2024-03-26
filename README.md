# SQL_Assignment_7

## Sorgu Senaryoları

* Film Tablosunu Rating Değerlerine Göre Gruplayın:

```bash
SELECT rating, COUNT(*) AS film_sayisi
FROM film
GROUP BY rating
ORDER BY rating;
```

Bu sorgu, film tablosundaki filmleri rating değerlerine göre gruplar ve her bir rating değeri için film sayısını gösterir.


* Replacement Cost'a Göre Film Sayısını Sıralayın:

```bash
SELECT replacement_cost, COUNT(*) AS film_sayisi
FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY film_sayisi DESC;
```

Bu sorgu, replacement_cost sütununa göre film sayısını gruplar ve film sayısı 50'den fazla olan replacement_cost değerlerini ve film sayılarını sıralar.


* Müşteri Sayılarını Store ID'ye Göre Sıralayın:

```bash
SELECT store_id, COUNT(*) AS musteri_sayisi
FROM customer
GROUP BY store_id
ORDER BY musteri_sayisi DESC;
```

Bu sorgu, customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını gösterir.


* En Fazla Şehir Barındıran Ülkeyi Bulun:

```bash
SELECT country_id, COUNT(*) AS sehir_sayisi
FROM city
GROUP BY country_id
ORDER BY sehir_sayisi DESC
LIMIT 1;
```

Bu sorgu, city tablosundaki şehir verilerini country_id sütununa göre gruplar ve en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını gösterir.

