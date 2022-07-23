t## Geocode search

```bash
curl --location --request POST 'http://localhost:4568/api/geocoding/search?q=ikeja&limit=5&format=json&addressdetails=1&zoom=17&polygon_geojson=1'
```


## Reverse Geocode search

```bash
curl --location --request POST 'http://localhost:4568/api/geocoding/reverse?lat=6.81670&lon=3.42691&format=json&zoom=17&addressdetails=1&polygon_geojson=1' \
--header 'Accept: application/json' \
--data-raw ''
```
