# Nomor 1
## Program
```MYSQL
SELECT orders.orderID,orders.orderDate,orders.CustID,
    -> customers.companyName,customers.contactName,Customers.City,
    -> customers.phone
    -> from orders,customers
    -> where (orders.custid=customerid);
```

## Hasil

![GAMBAR](aset/nomor1(7).png)
## Analisis
- `SELECT` digunakan untuk menentukan kolom-kolom mana yang ingin ditampilkan dalam hasil query.
- `orders.orderID`: Mengambil kolom `orderID` dari tabel `orders`.
- `orders.orderDate`: Mengambil kolom `orderDate` dari tabel `orders`.
- `orders.CustID`: Mengambil kolom `CustID` dari tabel `orders`.
- `customers.companyName`: Mengambil kolom `companyName` dari tabel `customers`.
- `customers.contactName`: Mengambil kolom `contactName` dari tabel `customers`.
- `customers.City`: Mengambil kolom `City` dari tabel `customers`.
- `customers.phone`: Mengambil kolom `phone` dari tabel `customers`.
- `FROM` digunakan untuk menentukan tabel mana yang akan diambil datanya
- `orders`: Merujuk ke tabel yang menyimpan data pesanan.
- `customers`: Merujuk ke tabel yang menyimpan data pelanggan.
- `WHERE` digunakan untuk menyaring baris-baris data yang diambil berdasarkan kondisi tertentu.
- `orders.custid = customers.customerid`: Kondisi ini menghubungkan tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai antara kolom `custid` di tabel `orders` dan `customerid` di tabel `customers`. Ini berarti hanya baris-baris yang memiliki `CustID` yang sama antara kedua tabel yang akan dimasukkan dalam hasil.

## Kesimpulan
 
 Query adalah perintah menggabungkan informasi dari dua tabel, yaitu `orders` dan `customers`. Query ini menghubungkan tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai di kolom `CustID` di `orders` dan kolom `customerID` di `customers`.

# Nomor 2
## Program
```MYSQL
SELECT o.OrderID,o.OrderDate,o.CustID,c.CompanyName,c.ContactName,c.City,
c.Phone FROM orders o,customers c WHERE o.CustID= c.CustomerID AND c.City="London";
```

## Hasil

![GAMBAR](aset/nomor1(7).png)
## Analisis
- `SELECT` digunakan untuk menentukan kolom-kolom mana yang ingin ditampilkan dalam hasil query.
- `o.OrderID`: Mengambil kolom `OrderID` dari tabel `orders`.
- `o.OrderDate`: Mengambil kolom `OrderDate` dari tabel `orders`.
- `o.CustID`: Mengambil kolom `CustID` dari tabel `orders`.
- `c.CompanyName`: Mengambil kolom `CompanyName` dari tabel `customers`.
- `c.ContactName`: Mengambil kolom `ContactName` dari tabel `customers`.
- `c.City`: Mengambil kolom `City` dari tabel `customers`.
- `c.Phone`: Mengambil kolom `Phone` dari tabel `customers`.
- `FROM` digunakan untuk menentukan tabel mana yang akan diambil datanya
- `orders o`: Tabel `orders` dengan alias `o`, yang menyimpan data pesanan.
- `customers c`: Tabel `customers` dengan alias `c`, yang menyimpan data pelanggan.
- `WHERE` digunakan untuk menyaring baris-baris data yang diambil berdasarkan kondisi tertentu.
- `o.CustID = c.CustomerID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai antara kolom `CustID` di tabel `orders` dan `CustomerID` di tabel `customers`.
- `c.City = "London"`: Menyaring data lebih lanjut, hanya mengambil baris-baris di mana nilai `City` di tabel `customers` adalah "London".

## Kesimpulan
 
 Query adalah perintah menggabungkan data dari tabel `orders` dan `customers` berdasarkan nilai `CustID` dan `CustomerID`, kemudian menyaring hasilnya untuk hanya menampilkan pesanan yang berasal dari pelanggan yang berada di London. Data yang diambil meliputi informasi pesanan seperti `OrderID`, `OrderDate`, dan `CustID`, serta informasi pelanggan seperti `CompanyName`, `ContactName`, `City`, dan `Phone`.

# Nomor 3
## Program
```MYSQL
SELECT o.OrderID,o.OrderDate,o.CustID,c.CompanyName,c.ContactName,c.City,
c.Phone FROM orders o,customers c WHERE o.CustID= c.CustomerID AND c.City="London";
```

## Hasil

![GAMBAR](aset/nomor1(7).png)
## Analisis
- `SELECT` digunakan untuk menentukan kolom-kolom mana yang ingin ditampilkan dalam hasil query.
- `o.OrderID`: Mengambil kolom `OrderID` dari tabel `orders`.
- `o.OrderDate`: Mengambil kolom `OrderDate` dari tabel `orders`.
- `c.CompanyName`: Mengambil kolom `CompanyName` dari tabel `customers`.
- `c.ContactName`: Mengambil kolom `ContactName` dari tabel `customers`.
- `c.Phone`: Mengambil kolom `Phone` dari tabel `customers`.
- `e.LastName`: Mengambil kolom `LastName` dari tabel `employees`.
- `e.Title`: Mengambil kolom `Title` dari tabel `employees`.
- `FROM` digunakan untuk menentukan tabel mana yang akan diambil datanya
- `orders o`: Tabel `orders` dengan alias `o`, yang menyimpan data pesanan.
- `customers c`: Tabel `customers` dengan alias `c`, yang menyimpan data pelanggan.
- `employees e`: Tabel `employees` dengan alias `e`, yang menyimpan data karyawan..
- `WHERE` digunakan untuk menyaring baris-baris data yang diambil berdasarkan kondisi tertentu.
- `o.CustID = c.CustomerID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai antara kolom `CustID` di tabel `orders` dan `CustomerID` di tabel `customers`.
- `o.EmpID = e.EmpID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `employees` berdasarkan kesamaan nilai antara kolom `EmpID` di tabel `orders` dan `EmpID` di tabel `employees`.

## Kesimpulan

 Query adalah perintah mengambil dan menampilkan informasi lengkap tentang pesanan (`OrderID`, `OrderDate`), informasi pelanggan (`CompanyName`, `ContactName`, `Phone`), serta informasi karyawan yang menangani pesanan tersebut (`LastName`, `Title`). Query ini menggabungkan data dari tiga tabel (`orders`, `customers`, dan `employees`) berdasarkan relasi antara ID pelanggan (`CustID` dan `CustomerID`) dan ID karyawan (`EmpID`).

# Nomor 4
## Program
```MYSQL
select o.orderID,o.orderDate,c.companyName,c.contactname,c.phone,e.lastname,e.title
-> from orders o,customers c,employes e
-> where o.custid=c.customerid AND o.empid=e.empid AND
-> e.firstname="margaret";
```

## Hasil

![GAMBAR](aset/nomor4(7).png)
## Analisis
- `SELECT` digunakan untuk menentukan kolom-kolom mana yang ingin ditampilkan dalam hasil query.
- `o.OrderID`: Mengambil kolom `OrderID` dari tabel `orders`.
- `o.OrderDate`: Mengambil kolom `OrderDate` dari tabel `orders`.
- `c.CompanyName`: Mengambil kolom `CompanyName` dari tabel `customers`.
- `c.ContactName`: Mengambil kolom `ContactName` dari tabel `customers`.
- `c.Phone`: Mengambil kolom `Phone` dari tabel `customers`.
- `e.LastName`: Mengambil kolom `LastName` dari tabel `employees`.
- `e.Title`: Mengambil kolom `Title` dari tabel `employees`.
- `FROM` digunakan untuk menentukan tabel mana yang akan diambil datanya
- `orders o`: Tabel `orders` dengan alias `o`, yang menyimpan data pesanan.
- `customers c`: Tabel `customers` dengan alias `c`, yang menyimpan data pelanggan.
- `employees e`: Tabel `employees` dengan alias `e`, yang menyimpan data karyawan.
- `WHERE` :digunakan untuk menyaring baris-baris data yang diambil berdasarkan kondisi tertentu.
- `o.CustID = c.CustomerID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai antara kolom `CustID` di tabel `orders` dan `CustomerID` di tabel `customers`.
- `o.EmpID = e.EmpID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `employees` berdasarkan kesamaan nilai antara kolom `EmpID` di tabel `orders` dan `EmpID` di tabel `employees`.
- `AND`:untuk menyeleksi dua data atau lebih pada perintah where 
- `e.firstName="Margaret"`: data pada kolom first dalam tabel employes harus berisi data "margaret" agar bisa tampil.

## Kesimpulan

 Query adalah perintah mengambil dan menampilkan mengambil data pesanan, informasi pelanggan, dan detail karyawan dari tiga tabel, dan hanya menampilkan hasil untuk karyawan bernama "Margaret".

# Nomor 5
## Program
```MYSQL
select o.orderID,o.orderDate,c.companyName,c.contactname,c.phone,e.lastname,e.title
-> from orders o,customers c,employes e
-> where o.custid=c.customerid AND o.empid=e.empid AND
-> e.firstname="margaret";
```

## Hasil

![GAMBAR](aset/nomor4(7).png)
## Analisis
- `SELECT` digunakan untuk menentukan kolom-kolom mana yang ingin ditampilkan dalam hasil query.
- `o.OrderID`: Mengambil kolom `OrderID` dari tabel `orders`.
- `o.OrderDate`: Mengambil kolom `OrderDate` dari tabel `orders`.
- `c.CompanyName`: Mengambil kolom `CompanyName` dari tabel `customers`.
- `c.ContactName`: Mengambil kolom `ContactName` dari tabel `customers`.
- `c.Phone`: Mengambil kolom `Phone` dari tabel `customers`.
- `e.LastName`: Mengambil kolom `LastName` dari tabel `employees`.
- `e.Title`: Mengambil kolom `Title` dari tabel `employees`.
- `FROM` digunakan untuk menentukan tabel mana yang akan diambil datanya
- `orders o`: Tabel `orders` dengan alias `o`, yang menyimpan data pesanan.
- `customers c`: Tabel `customers` dengan alias `c`, yang menyimpan data pelanggan.
- `employees e`: Tabel `employees` dengan alias `e`, yang menyimpan data karyawan.
- `WHERE` :digunakan untuk menyaring baris-baris data yang diambil berdasarkan kondisi tertentu.
- `o.CustID = c.CustomerID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `customers` berdasarkan kesamaan nilai antara kolom `CustID` di tabel `orders` dan `CustomerID` di tabel `customers`.
- `o.EmpID = e.EmpID`: Kondisi ini menghubungkan baris-baris dari tabel `orders` dengan tabel `employees` berdasarkan kesamaan nilai antara kolom `EmpID` di tabel `orders` dan `EmpID` di tabel `employees`.
- `AND`:untuk menyeleksi dua data atau lebih pada perintah where 
- `e.firstName="Margaret"`: data pada kolom first dalam tabel employes harus berisi data "margaret" agar bisa tampil.

## Kesimpulan

 Query adalah perintah mengambil dan menampilkan mengambil data pesanan, informasi pelanggan, dan detail karyawan dari tiga tabel, dan hanya menampilkan hasil untuk karyawan bernama "Margaret".

