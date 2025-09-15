# Restaurant Manager; Description
Menu-driven CLI to manage a restaurant’s menu stored in nested JSON  
Done with normal criteria and challenge goals


# Features
- Sorting: by name, category, price, availability
- Inputted a GUI
- Input Validation:
  - Unique IDs on add
  - Price ≥ 0 (numeric)
  - Non-empty name and category
  - Graceful re-prompt on invalid menu choices
  - Warnings when updating/deleting a non-existent ID
- Export:
  - Export all / last results (view/search/sort) to CSV or TXT
  - Choose fields on which to include
- Submenus:
  - Main to Search then ID / Name / Category
  - Main to View then All / By Category
  - Main to Update then choose name / category / price / availability


## Structure
restaurant_manager/
├─ data/
│ └─ restaurant_data.json
├─ src/
│ ├─ menu_item.py # MenuItem (to_dict, from_dict, update, str)
│ ├─ restaurant.py # load/save JSON, CRUD, search, sort, export
│ ├─ utils.py # validators, sorting keys, export helpers, formatting
│ └─ main.py # CLI menus & user flow
└─ README.md

# Quick Example/Demonstration:
Welcome!
1) View  2) Search  3) Add  4) Update  5) Delete
6) Sort  7) Export  8) Save & Exit
Choose: 2
Search by: 1) ID  2) Name  3) Category
Enter: 2
Text: biry
Found: [9] Chicken Biryani (Entree) - $14.99 | In stock: True

Add Item
id: 30
name: Mango Lassi
category: Beverages
price: 4.99
in stock (y/n): y
Added: [30] Mango Lassi (Beverages) - $4.99 | In stock: True
Sort by: 1) name 2) price 3) availability 4) category
Order: 1) asc 2) desc
Saved sort result in session. You can Export → “Last Results”.

{
  "name": "Spice of Nations",
  "location": "1234 Maplewood St, Springfield IL",
  "cuisine": "Indian and Pakistani",
  "menu": [
    {
      "category": "Appetizer",
      "id": 1,
      "items": [
        {"id": 1, "name": "Samosas", "price": 5.99, "in_stock": true}
      ]
    }
  ]
}
# Collaboration:
Siddiqi: menu_item.py, restaurant.py, README.md
Georgii: main.py, utils.py, also created GUI and advanced details

