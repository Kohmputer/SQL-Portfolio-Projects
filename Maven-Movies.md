## Maven-Movies 

--  1. My partner and I want to come by each of the stores in person and meet the managers. 
Please send over the managers’ names at each store, with the full address 
of each property (street address, district, city, and country please).  
-- 

```sql -- Add 3 backticks followed by sql
SELECT 
	  staff.first_name AS manager_first_name,
    staff.last_name AS manager_last_name,
    address.address,
    address.district,
    city.city,
    country.country 
FROM store
LEFT JOIN staff on store.manager_staff_id = staff.staff_id
LEFT JOIN address ON store.address_id = address.address_id
LEFT JOIN city  ON address.city_id = city.city_id 
LEFT JOIN country ON city.country_id = country.country_id;
``` -- Add 3 backticks
