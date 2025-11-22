# haircare-test-1

Hair care test
this project have been developed to have better understanding about hair and also to choose the best chemicals and haircare brand according to your hair type
Many people are dealing with a lot of stress which can be one the reason for hairloss

Key features of the project
•	it informs you about the hair chemicals you should avoid for less breakage 
•	it tells you about chemicals that would suit you
•	it also suggests the brand that have products based on chemicals that would suit you                                 
hair_ingredients = {
    "dry": {
        "good": ["Argan Oil", "Shea Butter", "Glycerin", "Panthenol (Vitamin B5)"],
        "bad": ["Strong Sulfates (SLS, SLES)", "Alcohol", "Salt (Sodium Chloride)"],
        "brands": ["Moroccanoil", "SheaMoisture", "L'Oreal Elvive Extraordinary Oil"]
    },
    "frizzy": {
        "good": ["Keratin", "Silicones (Dimethicone)", "Coconut Oil", "Argan Oil"],
        "bad": ["Strong Sulfates", "Drying Alcohols", "Salt"],
        "brands": ["John Frieda Frizz Ease", "Garnier Fructis Sleek & Shine", "Keratin Complex"]
    },
    "oily": {
        "good": ["Tea Tree Oil", "Salicylic Acid", "Niacinamide", "Clay (Kaolin/Bentonite)"],
        "bad": ["Heavy Oils", "Thick Butters", "Silicones (can trap oil)"],
        "brands": ["Paul Mitchell Tea Tree", "Neutrogena Anti-Residue Shampoo", "The Body Shop Tea Tree"]
    },
    "dandruff": {
        "good": ["Zinc Pyrithione", "Ketoconazole", "Salicylic Acid", "Tea Tree Oil"],
        "bad": ["Heavy Oils", "Silicone buildup", "Strong Fragrances"],
        "brands": ["Head & Shoulders", "Nizoral", "Selsun Blue"]
    },
    "damaged": {
        "good": ["Keratin", "Protein Treatments", "Ceramides", "Amino Acids"],
        "bad": ["Harsh Sulfates", "Heat Styling Chemicals", "Peroxide (bleach)", "Alcohol-based sprays"],
        "brands": ["Olaplex", "Redken Extreme", "L'Oreal Protein Recharge"]
    }
}


user_input = input("Enter your hair condition(s), separated by commas (e.g., dry, frizzy): ").lower()
conditions = [c.strip() for c in user_input.split(",")]


combined_good = set()
combined_bad = set()
combined_brands = set()
invalid_conditions = []

for cond in conditions:
    if cond in hair_ingredients:
        combined_good.update(hair_ingredients[cond]["good"])
        combined_bad.update(hair_ingredients[cond]["bad"])
        combined_brands.update(hair_ingredients[cond]["brands"])
    else:
        invalid_conditions.append(cond)


if combined_good:
    print("\n Recommended Ingredients for your hair:")
    for ing in combined_good:
        print(f"- {ing}")

if combined_bad:
    print("\n Ingredients to Avoid for your hair:")
    for ing in combined_bad:
        print(f"- {ing}")

if combined_brands:
    print("\n Recommended Hair Product Brands:")
    for brand in combined_brands:
        print(f"- {brand}")

if invalid_conditions:
    print("\n No data available for condition(s):", ", ".join(invalid_conditions))
    print("Try: dry, frizzy, oily, dandruff, damaged")


