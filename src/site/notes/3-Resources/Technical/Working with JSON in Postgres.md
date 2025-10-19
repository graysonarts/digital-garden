---
{"dg-publish":true,"permalink":"/3-resources/technical/working-with-json-in-postgres/","tags":["postgres","json","quicktip"],"updated":"2025-10-18T21:23:29.081-07:00"}
---


## Append to a JSON array

```sql
UPDATE purchases SET items_purchased = items_purchased ||   
'{"name": "LG Ultrawide Monitor",  
        "price": 190,  
        "productid": 8}' ::jsonb  
WHERE id=1;
```
