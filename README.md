📉 PriceScouter – n8n Workflow

PriceScouter is an n8n
 workflow designed to track product prices (e.g., on CEL.ro) and notify you when they drop below a defined threshold.

🚀 Features
✅ Reads product list and price thresholds from Google Sheets
✅ Fetches product pages via HTTP Request
✅ Extracts product name and price using HTML Extract + normalization script
✅ Compares current price with the threshold

📲 Sends alerts to Telegram when the price is below threshold
📧 Sends an email (via Gmail) with the current price if the threshold is not met

🛠️ Workflow Steps
Cron – runs the workflow on a schedule (configurable)
Google Sheets – loads product URLs and target thresholds
Set – Config – prepares the request configuration
HTTP Request – fetches the product page
HTML Extract – Price – extracts the product price and name
Code – Normalize & Compare – cleans and parses price values, compares with threshold
IF – Price ≤ Threshold?
YES → Sends Telegram alert
NO → Sends Gmail message with the current price

Clone this repo or import the .json workflow into n8n
Configure OAuth2 credentials for:
Google Sheets
Gmail
Telegram Bot (via BotFather)
Update your Google Sheet with products and thresholds
Run manually or schedule execution with Cron
