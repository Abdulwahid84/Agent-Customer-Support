# Agent-Customer-Support

Streamlit customer support assistant powered by Langflow and the Datastax Astra API. The app provides a chat interface for support questions and two data tabs that expose sample product and order datasets.

## Features

- Chat with the support agent through a simple Streamlit UI.
- View sample product data from `sample_data/sample_products.csv`.
- View sample order data from `sample_data/sample_orders.csv`.
- Uses a Langflow flow endpoint to generate responses.

## Requirements

- Python 3.10 or newer.
- A valid Langflow/AstraDB application token.

## Setup

1. Create and activate a virtual environment.
2. Install dependencies with:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root and add your token:

```env
APP_TOKEN=your_astra_token_here
```

You can copy `.env.example` as a starting point.

## Run the app

```bash
streamlit run app.py
```

## Project Structure

- `app.py` - Streamlit entrypoint and Langflow API integration.
- `Langflow Customer Support Agent.json` - Flow configuration export.
- `sample_data/` - CSV files used by the data tabs.
- `sample_documents/` - Supporting documents for the assistant.
- `demo_video.mp4` and `demo_thumbnail.png` - Demo media assets.

## Notes

- The app expects `APP_TOKEN` to be available at runtime.
- If you update the Langflow flow or API identifiers, make the same changes in `app.py`.