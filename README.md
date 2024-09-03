
## Create Postgresql table

Simple table:

```sql
CREATE TABLE my_layer (id uuid DEFAULT gen_random_uuid() NOT NULL PRIMARY KEY, label text, the_geom geometry(Polygon, 2056));

INSERT INTO my_layer (label, the_geom) VALUES ('Le Lac', ST_GeometryFromText('Polygon ((2567181.92856511194258928 1204869.27227213000878692, 2564880.11235772212967277 1203444.33842946030199528, 2565991.87392727797850966 1201205.15667669335380197, 2567855.24895230773836374 1201800.18399561033584177, 2568512.9107258478179574 1204070.68297568871639669, 2567181.92856511194258928 1204869.27227213000878692))', 2056));
```

## Configure pg_service.conf

Give qgisserver the `pg_demo` pg_service

```
[pg_demo]
host=...
port=5432
user=...
password=...
```

## Load the project in LWC 3.8.0

* myAtlas.qgs
* myAtlas.qgs.cfg
* myAtlas_attachments.zip
* lite.sqlite
  
