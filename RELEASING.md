# Releasing the dataset

## Recreate the raw data from glottography-data

In case of upstream changes in glottography-data:
```shell
cldfbench download cldfbench_messineo2011aproximacion.py
```

## Recreate the CLDF data

```shell
cldfbench makecldf cldfbench_messineo2011aproximacion.py --glottolog-version v5.2
cldfbench cldfreadme cldfbench_messineo2011aproximacion.py
cldfbench zenodo --communities glottography cldfbench_messineo2011aproximacion.py
cldfbench readme cldfbench_messineo2011aproximacion.py
```

## Validation

```shell
cldf validate cldf
```

```shell
cldfbench geojson.validate cldf
20      valid features
24      valid speaker areas
```

```shell
cldfbench geojson.glottolog_distance cldf --format pipe
```

| ID | Distance | Contained | NPolys |
|:---------|-----------:|:------------|---------:|
| anga1316 | 1.07 | False | 1 |
| ayor1240 | 0.00 | True | 3 |
| cham1315 | 0.00 | True | 1 |
| iyow1239 | 0.26 | False | 2 |
| maca1260 | 0.05 | False | 2 |
| moco1246 | 0.00 | False | 2 |
| niva1238 | 1.00 | False | 1 |
| nort2971 | 0.00 | True | 1 |
| pila1245 | 1.82 | False | 1 |
| sana1298 | 0.00 | False | 1 |
| sout2989 | 0.00 | True | 2 |
| tapi1253 | 0.01 | False | 1 |
| tere1279 | 6.56 | False | 1 |
| toba1269 | 1.59 | False | 4 |
| vile1241 | 2.59 | False | 1 |
| wich1264 | 0.00 | True | 1 |
