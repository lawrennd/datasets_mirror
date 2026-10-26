# UK apartment prices (HM Land Registry monthly Price Paid, 2012)

Contemporaneous monthly Price Paid Data (PPD) releases for February–October 2012, recovered from the Internet Archive. These are the files Hensman, Fusi and Lawrence (2013) downloaded for the apartment-price experiment in *Gaussian Processes for Big Data*, UAI 2013, §4.2.

The current Land Registry yearly snapshot (`pp-2012.csv`) is a later revision of the same register. It does not match the monthly files that were public in late 2012 / early 2013. This folder keeps those monthly releases so reconstructions can choose among them.

## Contents

`monthly_2012/` holds one CSV per lodgement month, renamed `YYYY-MM.csv`. Original Land Registry filenames are in the table below.

The files are the official monthly PPD as published (15 columns, including Record Status). They are not a derived extract: apartments vs houses, date windows, COU vs F+A, and postcode geocoding are left to the consumer.

Encoding is mixed. February 2012 has a header row. July 2012 contains a `£` as latin-1 `0xa3`. Dates mix ISO and `DD/MM/YYYY`.

## Provenance

Listed on the January 2013 data.gov.uk dataset page
[land-registry-monthly-price-paid-data](https://web.archive.org/web/20130127041544/http://data.gov.uk/dataset/land-registry-monthly-price-paid-data)
as downloads from `http://www.landregistry.gov.uk/__data/assets/file/...`.

Captures are the earliest Wayback snapshot still available for each file, preferring October 2012 so later replacements are not used. The October CSV itself was only archived in April 2013. A later June capture is larger than the October 2012 file; this mirror keeps the October 2012 June release.

| File | Original name | Wayback timestamp | Original URL |
|---|---|---|---|
| `monthly_2012/2012-02.csv` | `ppms.csv` | `20121007175146` | http://www.landregistry.gov.uk/__data/assets/file/0017/4292/ppms.csv |
| `monthly_2012/2012-03.csv` | `PPMS_0312.csv` | `20121007175436` | http://www.landregistry.gov.uk/__data/assets/file/0014/6602/PPMS_0312.csv |
| `monthly_2012/2012-04.csv` | `ppms-april-with-columns.csv` | `20121004172350` | http://www.landregistry.gov.uk/__data/assets/file/0015/11490/ppms-april-with-columns.csv |
| `monthly_2012/2012-05.csv` | `ppms-may-with-columns.csv` | `20121007174936` | http://www.landregistry.gov.uk/__data/assets/file/0017/13661/ppms-may-with-columns.csv |
| `monthly_2012/2012-06.csv` | `ppms-june-with-columns.csv` | `20121007175256` | http://www.landregistry.gov.uk/__data/assets/file/0019/18307/ppms-june-with-columns.csv |
| `monthly_2012/2012-07.csv` | `ppms-july-with-columns.csv` | `20121007175415` | http://www.landregistry.gov.uk/__data/assets/file/0003/21486/ppms-july-with-columns.csv |
| `monthly_2012/2012-08.csv` | `ppms-august-with-columns.csv` | `20121007175308` | http://www.landregistry.gov.uk/__data/assets/file/0020/23618/ppms-august-with-columns.csv |
| `monthly_2012/2012-09.csv` | `ppms-september-with-columns.csv` | `20121031132020` | http://www.landregistry.gov.uk/__data/assets/file/0013/26023/ppms-september-with-columns.csv |
| `monthly_2012/2012-10.csv` | `PPMS_update_31_Oct_2012_ew_csv_with-columns.csv` | `20130413003342` | http://www.landregistry.gov.uk/__data/assets/file/0008/28664/PPMS_update_31_Oct_2012_ew_csv_with-columns.csv |

Wayback bytes: `https://web.archive.org/web/{timestamp}id_/{original URL}`.

SHA-256 of the mirrored files:

```
137d462a87665153e5dd474858d7f82845f2f8c785d9361e771d46a336a37429  monthly_2012/2012-02.csv
9658a685083ed1610f39f678dfc4bed981304a0d9950ab07bc15fb34b3845f4c  monthly_2012/2012-03.csv
bc8fc42993871b9019696c925c76bb37cd13fe2e5f1681d7184e568c665a7839  monthly_2012/2012-04.csv
bc0e17d6301fc1cb66836f31bfba2c7a2ecbdc49e36c6f9237635d817b0aa3f7  monthly_2012/2012-05.csv
4ac3da476faa06a1b2af620e1cfa800ba757c53b2531ea4277f38ab9a4a29e6d  monthly_2012/2012-06.csv
bc2f6cd39e00f23a080bd6f1c262310e2dc7df33bcbb11431e5ac392d5d5b5c2  monthly_2012/2012-07.csv
bbba9891eeb19550ea4d63ed006d1ae98b1dcb64fe64ee4ad17afdf5db7b24f5  monthly_2012/2012-08.csv
32f39900eb77040792850b8503665d49df84a0a0fb79f9c49481879e7e573214  monthly_2012/2012-09.csv
b8c472b90715203a353d01ff2a12d0b4e09fd5f9e17df07ed250a4ed4fdd2a54  monthly_2012/2012-10.csv
```

## Licence

Contains HM Land Registry data © Crown copyright and database right 2012.
This data is licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
Contains Royal Mail data © Royal Mail copyright and database right 2012.
Contains National Statistics data © Crown copyright and database right 2012.

These files are the official Price Paid monthly publications. Address fields in them are subject to PAF terms in the original release; this mirror is of those publications, not a separately derived address product.

## Intended consumer

A `pods` loader in [lawrennd/ods](https://github.com/lawrennd/ods), analogous to `football_data`: callers choose month window, property-type filter, record-status filter, and geocoder rather than receiving a single reconstructed matrix.
