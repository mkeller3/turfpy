## Booleans Examples :
  * Boolean Within : Returns true if the first geometry is completely within the second geometry. The interiors of both geometries must intersect and, the interior and boundary of the primary (geometry a) must not intersect the exterior of the secondary (geometry b). 
  
| Argument  | Type | Description |
| ------- | ------ | ----------- |
| `feature1`  | Feature  | 	GeoJSON Feature or Geometry|
| `feature2`  | Feature | 	GeoJSON Feature or Geometry |

| Return  | Type | Description |
| ------- | ------ | ----------- |
| `boolean`  | bool  | True/False |

```python
from turfpy.booleans import boolean_within

point = {
    "type": "Feature",
    "properties": {},
    "geometry": {
    "coordinates": [
        -104.99089477656028,
        39.74071889567193
    ],
    "type": "Point"
    }
}
polygon = {
    "type": "Feature",
    "properties": {},
    "geometry": {
    "coordinates": [
        [
        [
            -105.50078324787434,
            39.94526320322274
        ],
        [
            -105.50078324787434,
            39.49578832519356
        ],
        [
            -104.31486287077342,
            39.49578832519356
        ],
        [
            -104.31486287077342,
            39.94526320322274
        ],
        [
            -105.50078324787434,
            39.94526320322274
        ]
        ]
    ],
    "type": "Polygon"
    }
}
boolean_within(point, polygon)
```