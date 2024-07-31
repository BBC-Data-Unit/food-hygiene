# Code

This folder contains Colab notebooks of Python code used in the project and a JSON file of steps followed in OpenRefine to identify duplicates.

First, conditional formatting was used in Excel to have a general view, then in OpenRefine this is the process followed:
 
1. Reorder spreadsheet so Lat column is sorted a – z, and select Reorder Rows Permanently.
2. Apply Duplicates facet to Lat and select True, so exact latitude figures will be ordered in consecutive rows.
3. Blank down cells in column BusinessName – this will identify two consecutive columns with the same BusinessName and then delete the name in the second row so it’s easier to filter later. The reasoning behind this is that we’ll probably then be able to detect rows with the same latitude and same business name, which could easily be duplicates.
4. Apply Facet by blank to column BusinessName.
5. Star these rows (732 in total) so they are easier to check later on, and then delete Facet by blank.
6. Sort a – z by BusinessName and drag Blanks (starred rows) so they are in top of the column.
7. Apply Text filter to column AddressLine1.
8. From here on, I’ve repeated this to do some random spot-checking:
  * Starting with the first row (number 1222.), I search its AddressLine1 (Bickels Yard Cafe ( Fusion )) in the Text filter box.
  * Two exact rows appear with the same latitude, so I flag the starred one (with the blank BusinessName), as Bickels Yard Cafe is clearly duplicated.
  * Reset AddressLine1 Text filter and repeat this process with other random rows.
 
Some cases found:
 
* Exact duplicates such as the one in row 1222 (Bickels Yard Cafe).
* Businesses (with the same BusinessName) that have changed their BusinessType and therefore have multiple rows. This is the case of rows 1259 and 1260 (Oasis Sandwich Bar), which changed from a “Sandwich shop” to a “Canteen”. It got a 3 as RatingValue in 2022, and now it’s awaiting inspection.
* Businesses that have NOT changed their BusinessType, but have been inspected more than once in the past few years, and therefore have different rows. This is the case of rows 11538 and 11537 (Mac’s cafe), which was inspected in March and August 2023 - and got different ratings (3 and 5).
* Businesses that have NOT changed their BusinessType, and have already been inspected, but now are awaiting inspection again, so therefore have different rows. This is the case of rows 8199 and 8198 (Merchants Tea Rooms), which had an inspection in 2022, and now is awaiting another inspection.


