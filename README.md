# zoomcamp_hw_1

### For question 3
SQL query:
```
SELECT lpep_pickup_datetime
FROM tripdata
WHERE trip_distance IN (SELECT MAX(trip_distance) FROM tripdata);
```
