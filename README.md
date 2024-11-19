# Chatbot

**Slack Stock Price Chatbot:**

A Python-based Slack chatbot that listens to user events in Slack channels and fetches the closing price of a stock symbol using the Alpha Vantage API. The bot responds with the requested stock's closing price directly in the Slack channel.

**Features**
**Real-Time Slack Integration:** Listens for messages in Slack channels.
**Stock Price Fetching:** Retrieves stock closing prices from Alpha Vantage.
**Secure API Integration:** Uses environment variables for sensitive tokens.

**Setup and Installation**
**1. Clone the Repository**
bash
Copy code
git clone https://github.com/your-username/slack-stock-bot.git
cd slack-stock-bot
**2. Set Up Python Environment**
Create a virtual environment:

bash
Copy code
python -m venv venv
Activate the virtual environment:

Windows:
bash
Copy code
venv\Scripts\activate
macOS/Linux:
bash
Copy code
source venv/bin/activate
Install dependencies:

bash
Copy code
pip install -r requirements.txt
3. Set Up Environment Variables
Create a .env file in the project directory and add the following variables:

bash
Copy code
SLACK_BOT_TOKEN=your-slack-bot-token
SLACK_SIGNING_SECRET=your-slack-signing-secret
ALPHA_VANTAGE_API_KEY=your-alpha-vantage-api-key
Replace your-slack-bot-token, your-slack-signing-secret, and your-alpha-vantage-api-key with your actual credentials.

**4. Set Up Slack App**
Create a Slack App:

Visit Slack API and create a new app.
Enable the Events API and set up a request URL (e.g., using ngrok for local testing).
Subscribe to these events:
message.channels
app_mention
Add OAuth Scopes:
chat:write
channels:history
app_mentions:read
Install the app to your workspace and copy the Bot Token and Signing Secret.

Usage
Run the Bot
Start your local Flask server:

bash
Copy code
python app.py
If using ngrok, expose the server:

bash
Copy code
ngrok http 5000
Set the ngrok URL as the request URL in your Slack app's settings.

Test the bot by typing a message in Slack:

Example: Close price of IBM?
Sample Commands
What is the close price for $AAPL?
Get me the closing price of $GOOG.
Dependencies
Flask - Web framework for handling Slack events.
Slack SDK - Integration with Slack APIs.
Requests - For making API calls to Alpha Vantage.
Install all dependencies using:

bash
Copy code
pip install -r requirements.txt
Project Structure
bash
Copy code
slack-stock-bot/
│
├── Chatbot.py             # Main application file
├── .env               # Environment variables (not included in repo)
├── README.md          # Documentation
Contributing
Fork the repository.
Create a feature branch:
bash
Copy code
git checkout -b feature-name
Commit your changes:
bash
Copy code
git commit -m "Add feature-name"
Push to the branch:
bash
Copy code
git push origin feature-name
Submit a pull request.


Contact
For any questions or issues, feel free to reach out:

Author: Divya Kodiyattil
Email: divya.kv0109@gmail.com
