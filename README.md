📈 Stock Ticker App (Java)

A real-time stock tracking application built in Java that fetches live market data and visualizes it in dynamic charts. Designed to demonstrate API integration, data processing, and real-time visualization.

✨ Demo Overview
⏱️ Queries live stock prices at fixed intervals
📊 Builds a time-series dataset in memory
📈 Generates charts every 20 data points
🖥️ Displays results in a live Swing window
🚀 Features
🔌 Live API Integration with Alpha Vantage
💰 High-precision pricing using BigDecimal
🧠 Efficient data handling via queue-based storage
📊 Real-time charting with XChart
🔁 Continuous streaming loop for live updates


🏗️ Architecture
[ Alpha Vantage API ]
          ↓
   HTTP Request (GET)
          ↓
   JSON Parsing (org.json)
          ↓
  Queue Storage (timestamp, price)
          ↓
 Chart Generation (XChart)
          ↓
   Swing Display Window

   
🛠️ Tech Stack
Category	Technology
Language	Java
Networking	HttpURLConnection
Data Parsing	org.json
Visualization	XChart
Data Type	BigDecimal


⚙️ Configuration

Modify these values in StockTickerApp.java:

String symbol = "DJI";   // Stock ticker symbol
int waitTimeMs = 5000;  // Delay between API calls


💡 Popular symbols:

AAPL – Apple
TSLA – Tesla
MSFT – Microsoft


🔧 Setup & Installation
1. Clone the repository
git clone https://github.com/your-username/your-repo.git
cd your-repo
2. Add dependencies

Download and include:

org.json
xchart

(Or use Maven/Gradle if preferred)

3. Get API Key

Create a free account at Alpha Vantage

Replace in code:

"&apikey=YOUR_API_KEY"

▶️ Running the App
javac StockTickerApp.java
java StockTickerApp

📊 Example Behavior
Every 5 seconds → fetch stock price
Every 20 data points → render chart
Opens a new window with updated visualization
