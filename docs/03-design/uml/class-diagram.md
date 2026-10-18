# Class Diagram — هوم‌استور

## ۱. مقدمه

این دیاگرام ساختار کلاس‌های اصلی سیستم را نشان می‌دهد.

## ۲. کلاس‌ها

### ۲.۱ Product
| ویژگی | نوع |
|--------|------|
| id | int |
| name | string |
| price | decimal |
| stock | int |
| category_id | int |
| brand | string |

### ۲.۲ Category
| ویژگی | نوع |
|--------|------|
| id | int |
| name | string |
| parent_id | int |

### ۲.۳ Customer
| ویژگی | نوع |
|--------|------|
| id | int |
| name | string |
| phone | string |
| address | string |

### ۲.۴ Order
| ویژگی | نوع |
|--------|------|
| id | int |
| customer_id | int |
| total_price | decimal |
| status | enum |

### ۲.۵ OrderItem
| ویژگی | نوع |
|--------|------|
| id | int |
| order_id | int |
| product_id | int |
| quantity | int |
| unit_price | decimal |

### ۲.۶ User (Admin)
| ویژگی | نوع |
|--------|------|
| id | int |
| email | string |
| password_hash | string |
| role | enum |

## ۳. روابط

- Category 1:N Product
- Customer 1:N Order
- Order 1:N OrderItem
- Product 1:N OrderItem
