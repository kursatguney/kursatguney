USE HastaneDb
GO

-- Filtreleme
----------------

--SELECT ad as [Bölüm Adý] 
--FROM Bolumler

--SELECT *
--FROM Doktorlar
--WHERE id=5

--SELECT * FROM Doktorlar WHERE adSoyad='tuna Sefer'
--SELECT * FROM Doktorlar WHERE adSoyad!='tuna sefer'
--SELECT * FROM Doktorlar WHERE adSoyad!='tuna sefer' AND adSoyad!='kevser tutku'
--SELECT * FROM Doktorlar WHERE id=3 OR id=5
--SELECT * FROM Doktorlar WHERE NOT adSoyad='tuna sefer'
--SELECT * FROM Doktorlar WHERE adres='Ýzmir' AND bolumId=5

--SELECT * FROM Doktorlar WHERE adSoyad LIKE 't%'
--SELECT * FROM Doktorlar WHERE adSoyad LIKE 'tut%'
--SELECT * FROM Doktorlar WHERE adSoyad LIKE '%evgar'
--SELECT * FROM Doktorlar WHERE adres LIKE '%a'
--SELECT * FROM Doktorlar WHERE adSoyad LIKE '%s%'
--SELECT * FROM Doktorlar WHERE adSoyad LIKE '_e%'
--SELECT * FROM Doktorlar WHERE adSoyad LIKE '__n%'

--Sýralama
----------
--SELECT * FROM Doktorlar ORDER BY adSoyad
--SELECT * FROM Doktorlar ORDER BY adSoyad DESC
--SELECT * FROM Doktorlar ORDER BY adres ASC, adSoyad DESC
--SELECT * FROM Doktorlar WHERE adres='Ýstanbul' ORDER BY adSoyad
--SELECT * FROM Doktorlar ORDER BY adSoyad WHERE adres='Ýstanbul' --yanlýþ 

--Hesaplamalar
--------------

USE Northwind
GO

--SELECT MIN(UnitPrice) as 'En Küçük Fiyat' FROM Products
--SELECT MAX(UnitPrice) as 'En Büyük Fiyat' FROM Products
--SELECT COUNT(*) as 'Ürün Sayýsý' FROM Products

--USE HastaneDb
--GO
--SELECT COUNT(*) - COUNT(bolumId) AS [Bölüme Atanmayan Doktor Sayýsý]  FROM Doktorlar
--SELECT COUNT(*) FROM Doktorlar WHERE bolumId IS NULL

--SELECT AVG(UnitPrice) AS [Ortalama Ürün Fiyatý] FROM Products
--SELECT SUM(UnitsInStock) FROM Products
--SELECT ProductName, UnitPrice, UnitsInStock, UnitPrice*UnitsInStock AS Total FROM Products
--SELECT SUM(UnitPrice*UnitsInStock) AS Total FROM Products

--Stringler
-----------
--SELECT ProductName, UPPER(ProductName), LOWER(ProductName) FROM Products
--SELECT ProductName, REPLACE(ProductName,'C','INFO TECH') AS SAÇMALIK FROM Products
--SELECT REPLACE(REPLACE(LOWER(ProductName), ' ','-'),'''','') AS PRODUCTURL FROM Products

USE HastaneDb
GO

--UPDATE Doktorlar SET adres='Bursa' WHERE id=3
--UPDATE Doktorlar SET bolumId=3 WHERE bolumId=5

DELETE FROM Doktorlar WHERE bolumId IS NULL


