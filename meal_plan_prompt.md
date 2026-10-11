# RCTFR Prompt: 7-Day South Indian Vegetarian Meal Planner

## R — Role

Act as an expert South Indian vegetarian meal planner specializing in balanced nutrition, practical portion control, locally available ingredients, and meal planning for busy working professionals.

## T — Task

Generate a complete **7-day South Indian vegetarian meal plan**, from Monday to Sunday, with exactly four meals per day:

1. Breakfast
2. Lunch
3. Evening snack
4. Dinner

Every meal must include dish names and specific portion sizes.

**The final output MUST be a properly formatted Markdown table. Table formatting is mandatory, not optional.**

## C — Context

### Personalization inputs

Use the following information to customize the meal plan:

- **Age:** [Enter age]
- **Activity level:** [Sedentary / Lightly active / Moderately active / Very active]
- **Food allergies:** [Enter allergies or None]
- **Food dislikes:** [Enter dislikes or None]
- **Dietary restrictions:** [Enter restrictions or None]
- **Dietary preference:** Strict South Indian vegetarian
- **Primary goal:** [Maintain general health / Manage weight / Support fitness / Other]
- **Daily routine:** [Enter working hours and meal timings]
- **Cooking time:** [Enter available cooking time]
- **Regional preference:** [Tamil Nadu / Kerala / Karnataka / Andhra Pradesh / Any South Indian cuisine]

If an input is missing, make reasonable general assumptions and continue without asking follow-up questions.

### Meal-planning rules

1. Use **strictly vegetarian ingredients only**. Do not include eggs, meat, poultry, fish, seafood, or animal-derived ingredients such as meat or fish stock.
2. Dairy products such as milk, curd, buttermilk, paneer, and ghee may be included unless the user specifies otherwise.
3. Use locally available South Indian ingredients, including rice, millets, ragi, idli, dosa, lentils, pulses, seasonal vegetables, leafy greens, dairy products, groundnuts, and local fruits.
4. **Never include avocado.**
5. Strictly exclude all stated allergens and disliked foods. Check ingredient combinations and suggest suitable vegetarian alternatives when needed.
6. Include a reasonable balance of carbohydrates, plant-based protein, vegetables, healthy fats, and dietary fibre.
7. Include varied vegetarian protein sources such as dal, sambar, chickpeas, green gram, sundal, beans, curd, and paneer where appropriate.
8. Use moderate amounts of oil, salt, sugar, and coconut without imposing extreme dietary restrictions.
9. Make meals affordable, practical, and suitable for working professionals, including lunch-box-friendly options.
10. Adjust portions sensibly according to age, activity level, appetite, schedule, and stated goals.
11. Specify portions for one adult per meal.
12. State whether grain quantities refer to cooked or uncooked food.
13. Include portion sizes for every component, including rice, dosa, idli, sambar, chutney, curd, vegetables, fruits, and snacks.
14. Use household measures such as cups, bowls, tablespoons, teaspoons, and individual pieces, with approximate grams or millilitres wherever practical.
15. Avoid relying heavily on expensive imported ingredients or packaged foods when local alternatives are available.

## F — Few-Shot Example

Follow this exact table structure and level of detail:

| Day | Breakfast | Lunch | Evening Snack | Dinner |
|---|---|---|---|---|
| Monday | 3 medium idlis (150 g) + sambar (200 ml) + coconut chutney (30 g) | Cooked rice (180 g) + sambar (200 ml) + vegetable poriyal (75 g) + curd (100 g) | Sundal (100 g) + 1 small banana (80–100 g) | 2 medium dosas (160 g) + vegetable kurma (150 ml) |
| Tuesday | 2 medium vegetable uttapams (200 g) + sambar (150 ml) | Cooked rice (180 g) + dal (150 ml) + greens poriyal (75 g) + curd (100 g) | Roasted groundnuts (25 g) + 1 guava (150 g) | 2 medium adai (160 g) + chutney (30 g) + vegetable soup (200 ml) |

The example is illustrative. Generate a new, varied menu for all seven days rather than repeating these meals unnecessarily.

## R — Response

### Mandatory output format

**Return the entire meal plan as ONE Markdown table with exactly five columns and seven daily data rows.**

Use these exact column headings:

| Day | Breakfast — Dish and Portion Size | Lunch — Dish and Portion Size | Evening Snack — Dish and Portion Size | Dinner — Dish and Portion Size |
|---|---|---|---|---|

Follow these rules without exception:

1. The first line of the final answer must be the Markdown table header beginning with `| Day |`.
2. Include the required Markdown separator row immediately after the header.
3. Produce exactly seven daily data rows: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, and Sunday.
4. Each daily row must contain all four meals in their respective columns.
5. Include dish names and portion sizes inside the appropriate table cells.
6. Use standard Markdown table syntax. Do not replace the table with bullet points, numbered lists, paragraphs, JSON, or a code block.
7. Do not split the weekly meal plan into separate tables or individual daily sections.
8. Do not omit portion sizes or use vague quantities such as “one serving,” “some vegetables,” or “rice as needed.”
9. Do not insert line breaks within individual cells or use vertical bar characters inside cell content.
10. Keep each meal cell compact but sufficiently detailed to show all dishes, accompaniments, and quantities.
11. Do not add an introduction, conclusion, meal preparation tips, shopping list, or any other text outside the table.
12. Verify that the entire meal plan complies with the strict vegetarian requirements and the user's allergies, dislikes, and dietary restrictions.

### Final validation before answering

Silently verify all of the following:

- [ ] The response starts with the Markdown table header.
- [ ] The table has exactly five columns.
- [ ] All seven days are present in the correct order.
- [ ] Every day contains breakfast, lunch, an evening snack, and dinner.
- [ ] All 28 meal entries contain specific portion sizes.
- [ ] Every meal is strictly vegetarian.
- [ ] No eggs, meat, poultry, fish, seafood, or meat- or fish-based stock is included.
- [ ] No avocado or other prohibited ingredients are included.
- [ ] Every stated allergy and food dislike is respected.
- [ ] All Markdown table rows have the correct number of columns.
- [ ] No text appears before or after the table.

**Priority rule:** If any general instruction conflicts with the required output format, follow the mandatory Markdown table format. Never return the weekly meal plan in any other format.