Initial Diagnosis


Problem: Exact duplicate row

Code: raw.duplicated().sum() returned 1

Planned Decision: Exclude the repeated copy after verification

Reason: The same observation appears twice and should not be counted twice.


Problem: Missing price

Code: raw["price"].isna().sum() returned 1

Planned Decision: Retain and flag

Reason: The missing price should not be replaced with an invented value.


Problem: Inconsistent item labels

Code: raw["item"].value_counts() showed both Oil B and oil b

Planned Decision: Correct

Reason: These appear to represent the same item but use different capitalization.


Problem: Price stored as text

Code: raw.info() showed the price column as string

Planned Decision: Correct

Reason: Prices need to be numeric for calculations and analysis.



Problem: Comma in price value

Code: Price value 1,250

Planned Decision:  correct/investigate

Reason: The comma may be a thousands separator. It should become 1250, but the unusual value should be checked.


Problem: Date stored as text

Code: raw.info() showed the date column as string

Planned Decision: Correct

Reason: Dates should be converted into a proper date format for time-based analysis.


