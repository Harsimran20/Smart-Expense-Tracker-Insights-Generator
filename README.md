# 💳 Expense Categorizer

A Python utility for automatically categorizing financial transactions based on merchant descriptions.

## 📋 Overview

This project provides a simple yet effective way to categorize expense transactions by analyzing the description field. The categorizer recognizes common merchants and assigns appropriate categories to help organize your financial data.

## ✨ Features

- 🚗 **Transport Detection**: Automatically identifies Uber transactions
- ☕ **Food & Beverage Detection**: Recognizes Starbucks purchases
- 🔍 **Case-Insensitive Matching**: Works regardless of text capitalization
- 📊 **Pandas Integration**: Seamlessly works with DataFrame operations
- 🏷️ **Fallback Category**: Assigns "Other" to unrecognized transactions

## 🚀 Usage

```python
import pandas as pd

def categorize(desc):
    if "uber" in desc.lower(): 
        return "Transport"
    elif "starbucks" in desc.lower(): 
        return "Food"
    return "Other"

# Apply categorization to your DataFrame
df['Category'] = df['Description'].apply(categorize)
```

## 📊 Example

| Description | Category |
|-------------|----------|
| "UBER TRIP 12345" | Transport |
| "Starbucks Coffee" | Food |
| "Amazon Purchase" | Other |

## 🛠️ Requirements

- Python 3.x
- pandas

## 📦 Installation

pip install pandas

## 📄 License

This project is open source and available under the MIT License.

---
