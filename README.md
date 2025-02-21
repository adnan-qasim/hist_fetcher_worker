# hist_fetcher_worker

## Overview

`hist_fetcher_worker` is a FastAPI-based API that fetches historical prices of cryptocurrencies from a specified website and returns the rates. This API allows users to query historical price data for various cryptocurrencies.

## Features

- Fetch historical price data for multiple cryptocurrencies.
- Return historical rates in a structured JSON format.
- Easy to use and integrate with other applications.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/hist_fetcher_worker.git
    cd hist_fetcher_worker
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. Start the FastAPI server:
    ```sh
    uvicorn main:app --reload
    ```

2. Access the API documentation at `http://127.0.0.1:8000/docs`.

## API Endpoints

### Fetch Historical Price

- **URL:** `/historical-price`
- **Method:** `GET`
- **Query Parameters:**
  - `coin`: The symbol of the cryptocurrency (e.g., `BTC`, `ETH`).
  - `date`: The date for which to fetch the historical price (format: `YYYY-MM-DD`).

- **Response:**
  ```json
  {
    "coin": "BTC",
    "date": "2023-01-01",
    "price": 45000.00
  }