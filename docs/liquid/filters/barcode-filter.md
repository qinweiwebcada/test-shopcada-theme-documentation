# Barcode Filter

### order\_barcode

Output img tag for the order id barcode, for Shopcada POS use.

```
{{ order.order_id | order_barcode }}
```

### shipment\_barcode

Output img tag for the package barcode, for Shopcada POS use.

```
{{ package.shipment_id | shipment_barcode }}
```

### customer\_barcode

Output img tag for the customer uid barcode, for Shopcada POS use.

```
{{ customer.customer_id | customer_barcode }}
```

### barcode

Output img tag for the barcode

```
{{ "text-to-generate-barcode" | barcode }}
```

### QR Code

Output img tag for the qr code

```
{{ "package.shipment_id" | qr_code }}
```
