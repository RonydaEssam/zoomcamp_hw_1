# Zoomcamp Module 1 HW

### For question 3
SQL query:
```SELECT 
   COUNT(CASE WHEN trip_distance <= 1 THEN 1 END) AS "Up to 1 mile",
   COUNT(CASE WHEN trip_distance > 1 AND trip_distance <= 3 THEN 1 END) AS "Between 1 and 3 miles",
   COUNT(CASE WHEN trip_distance > 3 AND trip_distance <= 7 THEN 1 END) AS "Between 3 and 7 miles",
   COUNT(CASE WHEN trip_distance > 7 AND trip_distance <= 10 THEN 1 END) AS "Between 7 and 10 miles",
   COUNT(CASE WHEN trip_distance > 10 THEN 1 END) AS "Over 10 miles"
FROM 
    tripdata
WHERE
	lpep_pickup_datetime LIKE '%2019-10%';
```

### For question 4
SQL query:
```
SELECT lpep_pickup_datetime
FROM tripdata
WHERE trip_distance IN (SELECT MAX(trip_distance) FROM tripdata);
```

