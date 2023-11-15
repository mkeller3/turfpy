Bbox
=====
Generate bounding box coordinates for given geojson.

Example
-------

.. jupyter-execute::

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
