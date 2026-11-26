# Who should a telecom operator help first?

This GCI World final project asks how an anonymised telecom operator could use a limited number of customer support slots. The proposal ranks customers who have experienced dropped or blocked calls and outlines a pilot to measure whether offering proactive technical support improves retention.

**At the same 400-contact quota, logistic regression identified 250 customers who later churned. Ranking by call failure share alone identified 219.**

[Presentation PDF](company_a_retention_slides.pdf) · [Analysis notebook](company_a_retention.ipynb) · [Assignment brief and submission checklist](ASSIGNMENT.md)

## From 100,000 customer records to a contact shortlist

Joining the course's customer profiles and usage records by customer ID yielded 100,000 matches. Among customers with at least 20 mean call attempts, those with a call failure share above 10% had **4.6 to 5.0 percentage points higher observed churn** within each of the three tenure groups. The differences stayed positive across all 27 combinations of tenure and screening cutoffs tested.

The contact shortlist came from 15,967 customers who met the two screening cutoffs. Both rankings were evaluated on the same 3,992 held-out customers using a fixed quota of 400 contacts.

| Ranking method | Customers who later churned in the 400 slots | Precision at quota | ROC AUC |
| --- | ---: | ---: | ---: |
| Call failure share | 219 | 54.75% | 0.511 |
| Logistic regression | 250 | 62.50% | 0.575 |

The model's precision gain was 7.75 percentage points, with a 95% paired bootstrap interval of +2.00 to +13.75 points. Overall ranking performance was modest. Nearly half of the historical sample carries the churn label. The operator would need to confirm live shortlist churn and the economics using recent data.

## What the operator could test

Offer shortlisted customers an SMS invitation to check their device, SIM, or connection. Randomise shortlisted customers between the offer and usual support, and compare churn on days 31 to 60. Under the stated cost and margin assumptions, breaking even requires **33 additional customers retained per 1,000 outreach assignments**. The proposed pilot would measure whether retention gains cover the actual outreach costs.

The assignment gives no location for Company A. Indonesia serves as a market comparison. Telkom's FY2025 filing gives market size and competition context, and its results announcement links Telkomsel's focus on network quality to reducing customer switching. [Telkom FY2025 Form 20-F](https://www.telkom.co.id/minio/show/data/lampiran/1778861459016_original_PERUSAHAAN-PERSEROAN-PERSERO-PT-TELEKOMUNIKASI-INDONESIA-TBK-20260515-20-F-EDGAR.pdf) · [Telkom FY2025 results](https://www.telkom.co.id/sites/berita/id_ID/news/laporan-keuangan-telkom-tahun-buku-2025-telkom-telkom-bukukan-kinerja-fy25-resilience-perkuat-fundamental-dan-hasilkan-total-shareholder-return-357-3767)

## Run the notebook

The notebook includes the executed tables and charts. To rerun it, use the two CSVs distributed with the course. Keep them in the original course folder and set `DATA_DIR` in the first code cell, or put your local copies in this layout.

~~~
telecom/
  Client.csv
  Record.csv
~~~

From the project folder, install the dependencies and open JupyterLab.

~~~sh
python -m pip install jupyterlab pandas numpy scipy scikit-learn matplotlib
python -m jupyter lab
~~~

Open [company_a_retention.ipynb](company_a_retention.ipynb) and run the cells in order. The notebook was verified locally with Python 3.14.7 and prints its analysis-library versions in the first code cell.
