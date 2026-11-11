## 3. CHECK## 3. CHECK

### Before and After Comparison

| Measure | Before Cleaning | After Cleaning |
| Total rows | 97 | 96 |
| Columns | 6 | 6 |
| Missing prices | 1 | 1 |
| Exact duplicates | 1 | 0 |

### AI Code Verdicts

| AI's Decision | Verdict | Evidence |
|---|---|---|
| Remove exact duplicates | KEEP | One exact duplicate was removed (97 to 96 rows). |
| Standardize item names | KEEP | "oil b" was changed to "Oil B". |
| Remove commas from prices | KEEP | "1,250" became 1250. |
| Convert prices to numeric | KEEP | Prices were converted to numeric format; one missing value remained. |
| Convert dates to datetime | KEEP | Dates were successfully converted. |
| Remove missing prices | KEEP | The missing price was retained as NaN instead of inventing a value. |
| Remove repeated date-item-city records | KEEP | Both Oil B records were retained because their prices differed (108.5 and 318.0). |

### Item Counts After Cleaning

| Item | Observations |
|---|---:|
| Oil B | 25 |
| Pulse C | 24 |
| Staple A | 23 |
| Sweetener D | 24 |
| **Total** | **96** |

Only one exact duplicate was removed. No other valid observations were deleted. The missing price remained unchanged, while the item label and price containing a comma were corrected.

## 4. REFLECT

I agreed with most of the AI's cleaning decisions. I chose to retain the missing price and both records with different prices for the same date, item and city because neither should be deleted without further investigation.

These decisions were better supported by the evidence than automatically deleting incomplete or repeated records. Without the AI, I might have missed the inconsistent item label, the comma in the price and the conflicting records. This exercise taught me to verify AI-generated code rather than accept every cleaning decision blindly.

