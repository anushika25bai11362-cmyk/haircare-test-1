1)Project Title

HairCare Ingredient & Product Recommender 


2)Project Overview

This project is a simple, interactive **command-line Python application** that recommends suitable hair-care ingredients and product brands based on the user’s hair conditions. The tool categorizes common hair concerns—such as dry, oily, frizzy, dandruff-prone, or damaged hair—and provides a curated list of:

* Ingredients that are **beneficial**
* Ingredients that **should be avoided**
* Reputable **hair product brands** for those conditions

The script also handles multiple conditions at once (e.g., *dry + frizzy*) by merging all relevant recommendations and notifying the user if any entered condition is not recognized


3)Features

Interactive user input-Users can type one or more hair conditions separated by commas.

Multiple-condition support-The script aggregates ingredient and brand recommendations across all conditions.

Structured recommendation system-For each condition, the program provides:

* **Good ingredients**
* **Ingredients to avoid**
* **Recommended brands**

Error handling for unknown conditions-Unknown or misspelled conditions are reported to the user.

Easy to expand

The hair_ingredients dictionary makes it simple to add new hair types or update product lists.

4)Technologies / Tools Used

* Python 3.x*
* Built-in Python features:

  * Dictionaries
  * Sets
  * User input handling
  * Looping & conditionals

(No external libraries required.)


5)Steps to Install & Run the Project

1. Install Python
Make sure Python 3.x is installed on your system.
You can check using:
2. Create a project folder
3. Add the Python script
Create a file named:
4. Run the program
5. Enter your hair conditions when prompted**

6)Instructions for Testing

Test 1: Single Valid Condition

Input:

```
dry
```

Expected behavior:

* Lists *good ingredients* for dry hair
* Lists *bad ingredients*
* Shows brand recommendations

---

Test 2: Multiple Valid Conditions

Input:

```
dry, frizzy
```

Expected behavior:

* Combines good & bad ingredients from both categories
* No duplicates (because sets are used)
* Combined brand list

---

Test 3: Unknown Condition

Input:

```
curly
```

Expected behavior:

* Program prints:
  `No data available for condition(s): curly`
* Suggests valid conditions

---

Test 4: Mixed valid + invalid

Input:

```
dry, curly, damaged
```

Expected behavior:

* Shows recommendations for *dry* and *damaged*
* Notifies:
  `No data available for condition(s): curly`



