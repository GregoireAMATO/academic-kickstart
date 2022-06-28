---
title: Finances
summary: Stock market portfolio management app
tags:
- Python
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
#external_link: "http://pydathon.pythonanywhere.com/"

image:
  # caption: Photo by rawpixel on Unsplash
  focal_point: Smart



# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

# Goals
When you have several different investment accounts, it can be complicated to manage your portfolio. That's why this application allows you to import directly your csv exports, to clean/enrich them, then to merge them automatically. The application has been developed with a "DCA" (Dollar Cost Averaging) investment perspective, and therefore with a long term regular investment perspective, so prices are updated every day, not in real time. 

## User guide
### Data cleaning 

First of all, you need to clean and enrich the data you want to study. To do this, use the first part at the top left of the application, select the source of the data if known, otherwise select "Standard", then launch the cleaning. This may take a few minutes, especially if your portfolio contains many lines. Be careful, if you are using a known export, make sure that no information other than your investments is included, as this could affect the import and the cleaning of the file. The only information needed is :

- The ISIN **AND/OR** the Symbol of the product necessarily, if you have both you can fill them in this will shorten the cleaning. For example, the ISIN of Apple is US0378331005 and its symbol is AAPL. Be careful, the ISIN of a product is unique but there can be confusion between symbols so be careful if you only enter the symbol of a stock. For example, L'Oreal, has the symbol OR (which also corresponds to Osisko Gold Royalties Ltd.) or OR.PA depending on the database, be careful and check that the result of the cleaning corresponds to what you have entered, and change the symbol if this is not the case. The application uses the Yahoo Finance API, so don't hesitate to go to the site if a line doesn't match in order to find the symbol associated with it.
- The average purchase price of the security(s)
- The quantity of securities held

The other information (symbol, price...) are deduced from the ISIN or the symbol, so it is not necessary to specify them. In order to help you, you will have at your disposal a template to download. Regarding crypto-currencies, the application is not yet compatible with them as they do not have an ISIN number, this will be added in the future. 

The access to data by API connection is under development and will be available soon. 

## Example of use

When you import your first file, a drop-down list appears, containing the names of all the files imported into the application. You can then select them to display a summary table. If you select multiple files (for example if you have multiple securities accounts on different platforms), they will be automatically merged.

The information and documents are stored in the application and are deleted at the end of each session. If you refresh the page, all documents will disappear.

The application is available [here](http://pydathon.pythonanywhere.com/).  