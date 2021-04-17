# Farm asset area

This module adds an `intrinsic_area` `decimal` field to assets which allows a
specific total area to be defined for assets. Farms that already have precise
area calculations may want to use this value instead of the total area
calculated from a coordinate based geometry system which is complex and not
always correct. The total area can be important when it is used in other
calculations such as the amount of fertilizer or water to apply to a field.

*This module is opinionated! A numeric `decimal` field (with a precision of 11
and scale of 4) is used so that `intrinsic_area` values can be aggregated in SQL
queries. These parameters should work fine for most agricultural fields, but
the total area of very large geometries may not work.*

## Maintainers:

Current maintainers:
- Paul Weidner (paul121) - https://github.com/paul121
