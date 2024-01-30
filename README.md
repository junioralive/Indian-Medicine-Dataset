# Indian Medicine Dataset

`TOTAL MEDICINES` `253973`

## Introduction
The Indian Medicine Dataset is a comprehensive collection of data about various medicines available in India. This dataset includes important details such as the medicine name, price, manufacturer, type, pack size, and composition. It is designed to be a valuable resource for researchers, healthcare professionals, and anyone interested in pharmaceuticals in India.

## Dataset Description
The dataset contains information on a range of medicines, with details that are crucial for understanding each product's specifics. The information includes the product ID, name, price in Indian Rupees (₹), discontinuation status, manufacturer's name, type of medicine (e.g., allopathy), pack size, and composition.

### Formats
The dataset is available in two formats:
1. **CSV (Comma-Separated Values)** - Ideal for importing into spreadsheet applications or processing with numerous data analysis tools.
2. **JSON (JavaScript Object Notation)** - Suitable for web applications and for use with modern programming languages.

### Data Fields
- **id**: Unique identifier for each medicine.
- **name**: Name of the medicine.
- **price(₹)**: Price of the medicine in Indian Rupees.
- **Is_discontinued**: Indicates whether the medicine is discontinued (FALSE = available).
- **manufacturer_name**: Name of the manufacturer.
- **type**: Type of medicine (e.g., allopathy).
- **pack_size_label**: Information about the size of the packaging.
- **short_composition1**: Primary composition of the medicine.
- **short_composition2**: Secondary composition of the medicine (if applicable).

## Data Example

### CSV Format

DOWLOAD : ```https://github.com/junioralive/Indian-Medicine-Dataset/blob/main/DATA/indian_medicine_data.csv```

```
id,name,price(₹),Is_discontinued,manufacturer_name,type,pack_size_label,short_composition1,short_composition2
1,Augmentin 625 Duo Tablet,223.42,FALSE,Glaxo SmithKline Pharmaceuticals Ltd,allopathy,strip of 10 tablets,Amoxycillin (500mg),Clavulanic Acid (125mg)
...
```

### JSON Format

DOWLOAD : ```https://github.com/junioralive/Indian-Medicine-Dataset/blob/main/DATA/indian_medicine_data.json```

```json
[
    {
        "id": "1",
        "name": "Augmentin 625 Duo Tablet",
        "price(₹)": "223.42",
        "Is_discontinued": "FALSE",
        "manufacturer_name": "Glaxo SmithKline Pharmaceuticals Ltd",
        "type": "allopathy",
        "pack_size_label": "strip of 10 tablets",
        "short_composition1": "Amoxycillin (500mg)",
        "short_composition2": "Clavulanic Acid (125mg)"
    },
    ...
]
```

## API Usage Example (THIS IS PRIVATE)
To insert data into the MongoDB using the Data API, you can use the following `requests` library:

```python
url = f'https://data.mongodb-api.com/app/{app_id}/endpoint/data/v1/action/findOne'

headers = {
    'Content-Type': 'application/json',
    'api-key': api_key
}

data = {
    "dataSource": "indianmedicinedata",
    "database": "indianmedicinedatabase",
    "collection": "indianmedicinedatabase",
    "filter": {
        "name": "Augmentin 625 Duo Tablet"
    }
}
response = requests.post(url, headers=headers, data=json.dumps(data))'
```

Replace `YOUR_APP_ID`, `YOUR_API_KEY`, `yourDatabase`, `yourCollection`, and the document content with your actual data.

## Usage and Contributions
This dataset is open for use by anyone interested in exploring Indian pharmaceutical products. I encourage contributions, especially in expanding the dataset, refining the existing data, and suggesting new ways to analyze and interpret the data.
