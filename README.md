# Flipkart Price Tracker with RSS
There are some nice open source trackers available for Price Tracking Flipkart products, none of them generated an 
RSS Feed.

## Output
Atom-formatted web feed with product's price, image URL and title.

## Inspiration
https://github.com/captn3m0/ideas#-amazon-price-tracker-with-rss
_It would be great if a similar bridge for Flipkart is added and hosted for free somewhere!._ Till then, run this script
before starting your RSS feed reader. For `newsboat`, it would be like:
```
newsboat() {
	echo "Initializing background process"
	/home/ritik/proj/flipkart_scraper/main.py > /dev/null 2>&1 &
	sleep 1
	command newsboat "$@"
	echo "Exiting"
	kill $!
}
```
in your rc file.