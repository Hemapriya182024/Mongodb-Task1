"# Mongodb-Task1" 


# MongoDB Queries Task README

## Dataset Description
The dataset used for this task is [product.json](https://github.com/rvsp/database/blob/master/mongodb/product.json). It contains information about various products stored in MongoDB.

## Queries Implemented

### 1. Find all the information about each product
```mongodb
db.products.find({})
```

### 2. Find the product price which are between 400 to 800
```mongodb
db.products.find({ price: { $gte: 400, $lte: 800 } })
```

### 3. Find the product price which are not between 400 to 600
```mongodb
db.products.find({ price: { $not: { $gte: 400, $lte: 600 } } })
```

### 4. List the four products which are greater than 500 in price
```mongodb
db.products.find({ price: { $gt: 500 } }).limit(4)
```

### 5. Find the product name and product material of each product
```mongodb
db.products.find({}, { name: 1, material: 1, _id: 0 })
```

### 6. Find the product with a row id of 10
```mongodb
db.products.find({ row_id: 10 })
```

### 7. Find only the product name and product material
```mongodb
db.products.find({}, { name: 1, material: 1, _id: 0 })
```

### 8. Find all products which contain the value "soft" in product material
```mongodb
db.products.find({ material: /soft/i })
```

### 9. Find products which contain product color "indigo" and product price 492.00
```mongodb
db.products.find({ color: "indigo", price: 492.00 })
```

### 10. Delete the products which have a product price value of 28
```mongodb
db.products.deleteMany({ price: 28 })
```

---
