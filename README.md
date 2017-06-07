# Description
An API that will query the house price index data and return an inflated price for a given property value and a region within the United Kingdom.

# Get it running
You will need to download the House Price Index Data from http://publicdata.landregistry.gov.uk/market-trend-data/house-price-index-data/UK-HPI-full-file-2016-05.csv and place it in the main folder. The application uses SQLite for performance reasons - therefore run `rake migrate` to translate the CSV file to SQLite (will take a couple of minutes)

## Server
`bundle install`

`rackup`

## Example Request
`http://localhost:9292/api/inflation?location=York&fromDate=2001-08-01&toDate=2016-05-01&propertyValue=100000`

Should Return similar to: `{"inflated_price":241570}`
