---
{"dg-publish":true,"permalink":"/atlas/working-with-json-in-postgres/","tags":["postgres","json","quicktip"],"noteIcon":"","updated":"2024-10-29T17:36:44.813-07:00"}
---


## Append to a JSON array

```sql
UPDATE purchases SET items_purchased = items_purchased ||   
'{"name": "LG Ultrawide Monitor",  
        "price": 190,  
        "productid": 8}' ::jsonb  
WHERE id=1;
```
