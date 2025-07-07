# How to Add Recipes to Your Bread Recipe Site

This guide explains how to add new recipes to your single-page bread recipe site, both manually and using the Recipe-to-HTML web tool.

---

## 1. Recipe Format: Plain Text Template

Write your recipes using this format:

```
Recipe Name: Cinnamon Rolls
Prep Time: 30 min
Bake/Cook Time: 25 min
Other Notes: Rise: 1h

Ingredients:
- 2 cups flour
- 1/4 cup sugar

Instructions:
1. Mix ingredients.
2. Let rise.
3. Bake.
```

---

## 2. Convert to HTML (Recommended)

### Use the Recipe-to-HTML Web Tool

1. **Open** `recipe-to-html.html` in your browser (on Android, Chrome or similar works great).
2. **Paste** your plain text recipe into the “Plain Text Recipe” textarea.
3. **Tap** the “Convert to HTML” button.
4. **Copy** the generated HTML from the output box.

---

## 3. Add the Recipe to Your Main Page

### a. Paste the Recipe Section

1. **Open** your main HTML file (`index.html`).
2. **Scroll down** to where the other recipes are.
3. **Paste** the new HTML `<section class="recipe" ...>` **below the last recipe section but above the closing `</body>` tag**.

   Example:
   ```html
   <section class="recipe" id="naan">
     <!-- Naan recipe here -->
   </section>

   <section class="recipe" id="cinnamon-rolls">
     <!-- Your new recipe from the converter -->
   </section>
   </body>
   </html>
   ```

### b. Update the Table of Contents

1. Find the `<nav>` section near the top of your HTML.
2. **Add a new entry** for your recipe:
   ```html
   <li><a href="#cinnamon-rolls">Cinnamon Rolls</a></li>
   ```
   Make sure the `href` matches the `id` in your recipe section.

---

## 4. Manual Method (Optional)

If you prefer, you can manually convert your plain text to HTML using this template:

```html
<section class="recipe" id="your-unique-id">
  <h2>Recipe Name</h2>
  <div class="meta">Prep: X min · Bake: Y min · [Other Notes]</div>
  <div class="ingredients">
    <strong>Ingredients:</strong>
    <ul>
      <li>item 1</li>
      <li>item 2</li>
    </ul>
  </div>
  <div class="instructions">
    <strong>Instructions:</strong>
    <ol>
      <li>Step one</li>
      <li>Step two</li>
    </ol>
  </div>
  <a href="#top" class="back-to-top">Back to Top ↑</a>
</section>
```

---

## 5. Tips

- **Section IDs:** Make sure each recipe’s `id` is unique and matches the Table of Contents link.
- **Order:** The order of recipes in the HTML file is the order they appear on the page.
- **Test:** Open your site in a browser after updating to make sure everything looks good and the links work.

---

## 6. Example: Adding a Recipe

1. **Write the plain text recipe:**
   ```
   Recipe Name: Cinnamon Rolls
   Prep Time: 30 min
   Bake/Cook Time: 25 min
   Other Notes: Rise: 1h

   Ingredients:
   - 2 cups flour
   - 1/4 cup sugar

   Instructions:
   1. Mix ingredients.
   2. Let rise.
   3. Bake.
   ```

2. **Use the Recipe-to-HTML tool** to convert and copy the HTML.

3. **Paste the HTML** into `index.html` as a new `<section class="recipe"...>`.

4. **Add to Table of Contents:**
   ```html
   <li><a href="#cinnamon-rolls">Cinnamon Rolls</a></li>
   ```

---

**Now you can quickly add new recipes from any device!**
