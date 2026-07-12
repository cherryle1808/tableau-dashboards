# Data Dictionary

The dataset consists of 6,380 transaction records from a fictional
Australian bookstore chain, covering both in-store and online sales
channels. It includes 29 variables describing key aspects of each
transaction — store location, customer profile, product details, pricing,
discounts, and payment methods. 
Financial measures such as gross sales, net
sales, and gross margin are also provided to support performance evaluation
and profitability analysis across customer segments, book categories, and
sales channels.

| Column Name | Description | Data Type |
|---|---|---|
| TransactionID | Unique transaction identifier | Identifier |
| OrderDate | Date of the transaction | Date/Time |
| Store | Bookstore branch or Online channel | Location |
| Channel | Sales channel (In-Store or Online) | Categorical |
| CustomerSegment | Customer segment classification | Categorical |
| Membership | Membership status (Member or Non-Member) | Categorical |
| CustomerState | Customer state/territory in Australia | Location |
| BookID | Unique identifier for each book | Identifier |
| Category | High-level category of the book | Categorical |
| Subcategory | Specific subcategory/genre of the book | Categorical |
| Publisher | Publisher of the book | Categorical |
| Format | Book format (Paperback, Hardcover, eBook, Audiobook) | Categorical |
| UnitPrice | Unit list price in AUD before discount | Number |
| Quantity | Number of units purchased in the transaction | Number |
| Promotion | Promotion code applied to the transaction | Categorical |
| DiscountRate | Discount rate applied based on promotion/membership | Number |
| ShippingFee | Shipping fee charged (if Online) | Number |
| GiftWrapFee | Gift wrap fee applied (if selected) | Number |
| GrossSales | Gross sales amount before discounts (UnitPrice × Quantity) | Number |
| DiscountAmount | Total discount amount applied | Number |
| NetSales | Net sales after discount, shipping, and gift wrap | Number |
| COGS | Cost of goods sold for the transaction | Number |
| GrossMargin | Gross margin (Net Sales – COGS) | Number |
| Returned | Flag for whether items were returned (1 = Yes, 0 = No) | Categorical |
| ReturnQty | Quantity of items returned | Number |
| ReturnAmount | Refund amount due to returns | Number |
| NetSalesAfterReturns | Net sales after subtracting returns | Number |
| GrossMarginAfterReturns | Gross margin after accounting for returns | Number |
| PaymentMethod | Payment method used by customers | Categorical |
