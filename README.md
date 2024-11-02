# Stock Alerts 📈

**Stock Alerts** is a Python application that provides users with real-time updates on stock movements and relevant news, helping them stay informed about potential changes in stock prices. By utilizing the AlphaVantage and NewsAPI, the project pulls essential stock and news data, calculates percentage changes, and sends SMS notifications to users via Twilio.

## Features

- **Real-Time Stock Tracking**: Uses the AlphaVantage API to pull today’s and previous day’s closing stock prices.
- **Market Movement Analysis**: Calculates the percentage change between today’s and yesterday’s closing prices to determine if the stock is trending up or down.
- **News Analysis**: Fetches relevant news articles for a given stock from the NewsAPI to help explain recent market movements.
- **SMS Notifications**: Sends SMS alerts directly to users with stock updates and news summaries using Twilio.

## Project Workflow

1. **Stock Price Fetching**:
   - The application uses AlphaVantage to retrieve the latest stock prices for the selected companies.
   - It calculates the price difference and percentage change to determine the stock’s direction (up or down).

2. **News Retrieval**:
   - Based on stock performance, the application uses NewsAPI to retrieve recent headlines for the relevant company.
   - This information helps users understand why the stock may have moved up or down.

3. **Notification via SMS**:
   - Using Twilio, users receive an SMS alert with stock performance details and a summary of relevant news articles.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/stock-alerts.git
   cd stock-alerts
   ```

3. **Set Up API Keys**:
   - **AlphaVantage API Key**: Sign up at [AlphaVantage](https://www.alphavantage.co/) to get an API key.
   - **NewsAPI Key**: Sign up at [NewsAPI](https://newsapi.org/) to get an API key.
   - **Twilio API Credentials**: Sign up at [Twilio](https://www.twilio.com/) to obtain your Account SID, Auth Token, and a Twilio phone number.

4. **Create a `.env` File**:
   Add your API keys and Twilio credentials to a `.env` file:
   ```plaintext
   ALPHAVANTAGE_API_KEY=your_alpha_vantage_api_key
   NEWSAPI_KEY=your_news_api_key
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   USER_PHONE_NUMBER=your_phone_number
   ```

## Usage

Run the main Python file to start receiving stock alerts:
```bash
python main.py
```

When executed, the script will:
1. Retrieve today’s and yesterday’s closing prices for the selected stock.
2. Calculate the percentage difference and determine if the stock is going up or down.
3. Fetch related news headlines to give context on why the stock might have changed.
4. Send an SMS notification to the user with the stock performance summary and top news highlights.

## Example SMS Alert

```
TSLA: 📉
-0.0860897145446297
Headline: Short-Seller Andrew Left Previews Defense in Skirmish Over 3,000 Extra Words.
Brief: (Bloomberg) -- Short seller Andrew Left is gearing up to seek dismissal of a US Securities and Exchange Commission lawsuit over his trading activities, with ...
```

## Dependencies

- [AlphaVantage API](https://www.alphavantage.co/) - For real-time stock price data
- [NewsAPI](https://newsapi.org/) - For fetching news related to the stock
- [Twilio API](https://www.twilio.com/) - For sending SMS notifications to users


---

