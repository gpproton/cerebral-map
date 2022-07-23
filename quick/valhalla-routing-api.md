## Valhalla routing API

```bash
curl --location --request POST 'http://localhost:4568/api/routing/route' \
--header 'Content-Type: application/json' \
--data-raw '{
    "locations": [
        {
            "lat": 6.81670,
            "lon": 3.42691
        },
        {
            "lat": 9.14494,
            "lon": 7.53636
        }
    ],
    "directions_type": "none",
    "costing": "truck",
	"costing_options": {
    "truck": {
        "shortest": true,
        "top_speed": 45,
        "weight": 40,
        "axle_load": 40,
        "gate_cost": 300,
        "use_highways": 1
    }
  }
}'
```
