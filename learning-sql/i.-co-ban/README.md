---
description: >-
  Bắt đầu đơn giản khi áp dụng các cú pháp đơn giản để truy xuất dữ liệu (Query
  data)
---

# 1. Cơ bản

## Các cú pháp cơ bản

#### SELECT

Lệnh **SELECT** dùng để xác định cột trong 1 bảng mà bạn muốn query đến

{% code title="Ví dụ" overflow="wrap" lineNumbers="true" %}
```sql
SELECT * // Chọn Tất cả
SELECT order_id // Chọn cột Mã đơn hàng (Order ID)
SELECT order_id, product_name // Có thể chọn nhiều cột bằng cách thêm dấu ","
```
{% endcode %}

#### FROM

Lệnh **FROM** dùng để chọn bảng dữ liệu mà bạn đang muốn truy xuất đến

{% code title="Ví dụ" overflow="wrap" lineNumbers="true" %}
```sql
SELECT * FROM sales // Chọn tất cả cột ở bảng Sales
```
{% endcode %}

#### WHERE

Lệnh **WHERE** dùng để thêm điều kiện lọc

{% code title="Ví dụ" overflow="wrap" lineNumbers="true" %}
```sql
SELECT *
FROM sales
WHERE 
    net_sale < 100000 // Giá sản phẩm < 100.000
    AND
    product_name = 'Car' // Có tên sản phẩm là 'Car'
    AND
    customer_name LIKE 'John%' // Tìm tên khách hàng bắt đầu bằng 'John'
```
{% endcode %}

#### ORDER BY

Lệnh **ORDER BY** dùng để sắp xếp kết quả theo tứ tự

{% code title="Ví dụ" overflow="wrap" lineNumbers="true" %}
```sql
SELECT *
FROM sales
WHERE 
    net_sale < 100000 // Giá sản phẩm < 100.000
    AND
    product_name = 'Car' // Có tên sản phẩm là 'Car'
    AND
    customer_name LIKE 'John%' // Tìm tên khách hàng bắt đầu bằng 'John'
ORDER BY ASC // Sắp xếp từ nhỏ đến lớn hoặc từ A đến Z
```
{% endcode %}

#### LIMIT

Cú pháp **LIMIT** dùng để giới hạn số dòng

{% code title="Ví dụ" overflow="wrap" lineNumbers="true" %}
```sql
SELECT *
FROM sales
WHERE 
    net_sale < 100000 // Giá sản phẩm < 100.000
    AND
    product_name = 'Car' // Có tên sản phẩm là 'Car'
    AND
    customer_name LIKE 'John%' // Tìm tên khách hàng bắt đầu bằng 'John'
ORDER BY ASC // Sắp xếp từ nhỏ đến lớn hoặc từ A đến Z
LIMIT 100 // Giới hạn 100 dòng
```
{% endcode %}
