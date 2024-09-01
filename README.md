<details>

<summary>Giriş</summary>

İlişkisel veritabanlarıyla etkileşim kurmak için standart SQL komutları CREATE, SELECT, INSERT, UPDATE, DELETE ve DROP'tur. Bu komutlar, yapılarına göre gruplara ayrılabilir:


<table>
  <thead>
    <tr>
    <th>Komut</th>
    <th>Açıklama</th>
    <th>Kullanım</th>
  </tr>
  </thead>
  <tbody>
    <tr>
    <td>CREATE</td>
    <td>Veritabanında yeni bir tablo, tablonun bir görünümü veya başka bir nesne oluşturur</td>
    <td>CREATE DATABASE testDB;</td>
  </tr>
    <tr>
    <td>ALTER</td>
    <td>Tablo gibi mevcut bir veritabanı nesnesini değiştirir.</td>
    <td>ALTER TABLE table_name {ADD|DROP|MODIFY} column_name {data_ype};</td>
  </tr>
    <tr>
    <td>DROP</td>
    <td>Veritabanındaki bir tablonun tamamını, bir tablonun görünümünü veya başka bir nesneyi siler.</td>
    <td>DROP DATABASE database_name;</td>
  </tr>
     <tr>
    <td>INSERT</td>
    <td>Kayıt Oluşturur</td>
    <td>INSERT INTO table_name( column1, column2....columnN) VALUES ( value1, value2....valueN);</td>
  </tr>
     <tr>
    <td>UPDATE</td>
    <td>Kaydı Günceller</td>
    <td>UPDATE table_name SET column1 = value1, column2 = value2....columnN=valueN [ WHERE CONDITION ];</td>
  </tr>
     <tr>
    <td>DELETE</td>
    <td>Kaydı siler</td>
    <td>DELETE FROM table_name WHERE {CONDITION};</td>
  </tr>
     <tr>
    <td>SELECT</td>
    <td>Kaydı getirir</td>
    <td>SELECT column1, column2....columnN FROM table_name;</td>
  </tr>
  </tbody>
</table>

</details>


-------------------------------------------------------------------------------

<details>

<summary>SELECT</summary>

***Tüm kayitlari getirir***

```sql
SELECT * FROM table_name;
```

***Tüm kayitlari belirtilen kolonlara gore getirir***

```sql
SELECT column1, column2....columnN FROM table_name;
```

***Farkli kayitlari getirir***

```sql
SELECT DISTINCT column1, column2....columnN FROM table_name;
```

***Belirtilen kosullara uyan kayitlari getirir***

```sql
SELECT column1, column2....columnN FROM table_name WHERE CONDITION;
```

***Ve/Veya kosulunu saglayan kayitlari getirir***

```sql
SELECT column1, column2....columnN FROM table_name WHERE CONDITION-1 {AND|OR} CONDITION-2; CHAPTER 4
```

***Belirtilen degerdeki kayitlari getirir***

```sql
SELECT column1, column2....columnN FROM table_name WHERE column_name IN (val-1, val-2,...val-N);
```

***Belirtilen araliktaki kayitlari getirir***

```sql
SELECT column1, column2....columnN FROM table_name WHERE column_name BETWEEN val-1 AND val-2;
```

***Belirtilen kolona gore kayitlari kucuten buyuge yada buyukten kucuge siralar***

```sql
SELECT column1, column2....columnN FROM table_name WHERE CONDITION ORDER BY column_name {ASC|DESC};
```

***Belirtilen kolona gore kayitlari gruplar***

```sql
SELECT SUM(column_name) FROM table_name WHERE CONDITION GROUP BY column_name;
```

***Kayit sayisini verir***

```sql
SELECT COUNT(column_name) FROM table_name WHERE CONDITION;
```


</details>
