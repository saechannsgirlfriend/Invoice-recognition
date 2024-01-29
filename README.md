# Invoice-recognition

This project, designed for RJY, focuses on extracting information from invoice photos. Supported file formats include .PDF, .JPG, and .PNG. I compared the performance of several OCR (Optical Character Recognition) APIs, including Google Image OCR, PDF OCR, and OCR Space API. Among these, OCR Space performed the best. Subsequently, I utilized regex (regular expressions) to extract information such as item names, amounts, and rates, and then returned this data in a dataframe format. Lastly, I applied fuzzy matching to align the inventory item lists with the extracted dataframe, enabling the retrieval of corresponding item codes.

### Functions Included
- ocrSpaceFile: Utilizes the OCR Space API to convert photos into text.
- extractString: Employs regex to identify details like date, invoice number, and company name.
- extractLines: Identifies lines containing item information within the text.
- itemInfo: Extracts amounts, prices, and item names from rows containing item information.
- matchingCode: Applies fuzzy matching to accurately find item codes based on item names.
