<div align="center">
  <img src="https://sltptr.github.io/static/images/LSSLogo.png" 
    alt="LSS Logo" style="max-width: 60%; width: 600px; height: auto;">
</div>

<p align="center">(but still simple)</p>

### Motivation

RSS is a great tool for getting your internet updates, and having used it for
the past year I wanted to see if there was a way to filter my feeds based on
data collected with click tracking. LSS is that solution, it's a simple
recommendation system that filters items through classifiers before publishing
them to your feed.

### Features

- Filter with a combination of TF-IDF Logistic Regression and DistilBERT
  classification.
- Toggle show all results from a feed, regardless of predictions.
- Set default and specific weighted predictions for each feed.

### Setup

1. Copy over the `config/default-config.yml` to `config/config.yml`, make
   changes as you'd like.
2. Create `.env`, add necessary envvars `SQLALCHEMY_URL` and `IAM_ROLE` (only if
   using DistilBERT).
3. Run `docker compose up --build -d`.
