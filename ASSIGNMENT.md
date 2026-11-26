# GCI World final assignment brief

This is a summary of the 2026 GCI World final assignment instructions and Company A data description supplied with the course.

## Consulting scenario

You are a new associate at an IT consulting firm. The firm has been commissioned to run a proof of concept for a client with a large historical dataset and limited in-house expertise for analysing it. Find a business problem that matters to the client, use the supplied data and external market research to investigate it, and present an actionable proposal with an estimate of business impact.

The assignment leaves the business problem and target variable up to the participant. This project asks whether a telecom operator can use call failure and other historical service signals to prioritise technical support outreach.

## What the proposal needs to show

1. Use exploratory data analysis (EDA) to identify a problem specific to the client.
2. Use cited external sources to explain the market context and support the choice of problem.
3. Build at least one appropriate machine learning or statistical model. State the model name, evaluation metric, and score in the slides. Explain the rationale, how you built it, and how its results inform the proposal.
4. Recommend a concrete action and quantify its expected impact, with assumptions for estimates the data cannot provide.
5. Use multiple visualisations and communicate the analysis in a way executives can understand.

## Supplied data

Company A is an anonymised telecommunications provider. Both tables contain one row per customer and can be joined through `Customer_ID`. In the supplied files, the join matches all 100,000 customer IDs.

| Source file | Contents |
| --- | --- |
| `Client.csv` | Account and subscriber history, devices, and customer profile attributes |
| `Record.csv` | Aggregate usage, billing, call quality, customer support activity, months in service, and the churn label |

The dictionary defines `churn` as leaving between 31 and 60 days after the observation date. The course also supplies a telecom tutorial notebook with an example of loading, joining, and analysing the two tables. Use course-distributed copies of the materials and data.

## Submission checklist

The deadline in the course README is **28 November 2026 at 11:30 UTC (18:30 WIB)**. The course accepts resubmissions until the deadline. Reattach the slides, notebook, and references each time. The latest complete submission is the one evaluated. [Omnicampus submission portal](https://edu.omnicamp.us/en/courses/170/reports/125/)

| Item | Course requirement | This project |
| --- | --- | --- |
| Slides | PDF, up to 15 slides including cover and references, maximum 10 MB | [11 slides, about 75 KB](company_a_retention_slides.pdf) |
| Notebook | Reproducible `.ipynb` or `.py`, or ZIP if multiple files | [Executed `.ipynb`](company_a_retention.ipynb) |
| Filename | Use your Omnicampus account name for the slides and notebook | Rename the submission copies to `OmnicampusAccountName.pdf` and `OmnicampusAccountName.ipynb` |
| References | Cite sources on the slides and enter matching citations in the Omnicampus References field | The entries below match the PDF |
| Generative AI | Include the AI chat history URL in References when used. The course evaluates your own analysis and synthesis | Add your actual chat URL and review and personalise the proposal before submission |

### References for Omnicampus

Enter one item per row, followed by your AI chat history URL.

1. GCI World final assignment materials. Company A Dataset Overview and course-supplied telecom dataset. Aggregate results from the companion analysis notebook, 2026.
2. PT Telkom Indonesia. FY2025 Form 20-F, Item 4B, p. 95. [Telkom filing](https://www.telkom.co.id/minio/show/data/lampiran/1778861459016_original_PERUSAHAAN-PERSEROAN-PERSERO-PT-TELEKOMUNIKASI-INDONESIA-TBK-20260515-20-F-EDGAR.pdf)
3. PT Telkom Indonesia. FY2025 results announcement, 12 May 2026. [Telkom results](https://www.telkom.co.id/sites/berita/id_ID/news/laporan-keuangan-telkom-tahun-buku-2025-telkom-telkom-bukukan-kinerja-fy25-resilience-perkuat-fundamental-dan-hasilkan-total-shareholder-return-357-3767)
4. Kementerian Komunikasi dan Digital. RAFI 2026 evaluation, 10 April 2026. [Komdigi release](https://portal.komdigi.go.id/kanal-publik/berita-kini/10145)
5. scikit-learn. [LogisticRegression documentation](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
6. Efron, B. (1979). Bootstrap Methods: Another Look at the Jackknife. The Annals of Statistics, 7(1), 1–26. [doi:10.1214/aos/1176344552](https://doi.org/10.1214/aos/1176344552)
