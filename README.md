# Medicare Inpatient Charges Public Data Set 2011-2014.

Sourced from the Google Cloud Public Data Set ["Medicare Data"](https://cloud.google.com/bigquery/public-data/medicare).

Query to generate output csv:

```sql
#standardSQL
SELECT *, 2011 as year FROM `bigquery-public-data.medicare.inpatient_charges_2011`
UNION ALL
SELECT *, 2012 as year FROM `bigquery-public-data.medicare.inpatient_charges_2012`
UNION ALL
SELECT *, 2013 as year FROM `bigquery-public-data.medicare.inpatient_charges_2013`
UNION ALL
SELECT *, 2014 as year FROM `bigquery-public-data.medicare.inpatient_charges_2014` ;
```

gzipped due to GitHub's 100MB file-size limit.
