🔷 HTML

📌 Basics

**1.What is HTML and what is it used for?**

<details>
  <summary>Answer:</summary>
  
**HTML** stands for **HyperText Markup Language** — it’s the **standard language** used to create and structure content on the web.

## **1. What it does**

* Defines the **structure** of a web page (headings, paragraphs, images, links, forms, etc.).
* Uses **tags** (elements) to mark up content so browsers know **what each part means**.
* Works together with:

  * **CSS** → for styling
  * **JavaScript** → for interactivity

## **2. Basic example**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My First Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is my first HTML page.</p>
</body>
</html>
```

* `<h1>` → heading
* `<p>` → paragraph

## **3. What it’s used for**

1. **Structuring content** — dividing text, images, and other media into meaningful sections.
2. **Linking documents** — using hyperlinks (`<a>`) to connect pages.
3. **Embedding media** — adding images, videos, audio.
4. **Building forms** — collecting user input for login, search, etc.
5. **Making content accessible** — through semantic tags for screen readers and SEO.

💡 **Interview tip:**
 *“Is HTML a programming language?”* →
No, it’s a **markup language** — it describes content but doesn’t contain logic or algorithms.

  
</details> 
   
**2.What is semantic HTML? Give examples.**

<details>
  <summary>Answer:</summary>

**Semantic HTML** means using HTML elements that **convey meaning** about their content and role, rather than just their appearance.

It helps:

* **Browsers** → understand the document’s structure.
* **Search engines** → improve SEO by knowing what’s important.
* **Assistive technologies** (screen readers) → improve accessibility.

## **1. Non-semantic vs semantic**

```html
<!-- Non-semantic -->
<div id="header"></div>
<div class="article"></div>

<!-- Semantic -->
<header></header>
<article></article>
```

Both can be styled the same, but the second example **tells browsers and assistive tools what the content is**.

## **2. Common semantic elements**

| Tag            | Meaning / Use                                                |
| -------------- | ------------------------------------------------------------ |
| `<header>`     | Introductory content or navigation for a page or section     |
| `<nav>`        | Navigation links                                             |
| `<main>`       | Main content (only one per page)                             |
| `<section>`    | Thematic grouping of content                                 |
| `<article>`    | Self-contained piece of content (e.g., blog post, news item) |
| `<aside>`      | Secondary content (e.g., sidebar)                            |
| `<footer>`     | Footer for a page or section                                 |
| `<figure>`     | Self-contained media (image, diagram, code block)            |
| `<figcaption>` | Caption for `<figure>`                                       |
| `<time>`       | Date or time                                                 |
| `<mark>`       | Highlighted text                                             |

## **3. Example in context**

```html
<header>
  <h1>My Blog</h1>
  <nav>
    <a href="/">Home</a>
    <a href="/about">About</a>
  </nav>
</header>

<main>
  <article>
    <h2>First Post</h2>
    <p>Welcome to my blog...</p>
  </article>
</main>

<footer>
  <p>&copy; 2025 My Blog</p>
</footer>
```

💡 **Interview tip:**
 *“Why use semantic HTML instead of `<div>` everywhere?”* →
Because it improves **accessibility, SEO, maintainability**, and helps machines understand the structure.

</details>

**3.What semantic tags do you know?**


<details>
  
  <summary>Answer:</summary>

Semantic HTML tags are elements whose names describe their meaning and role in the document, both for humans and machines (like browsers, search engines, and screen readers).

Here are the most common semantic tags:

### **Structural tags**

* `<header>` – top section of a page or a section, usually contains navigation or titles
* `<nav>` – navigation block with links
* `<main>` – the main content of the page (only one per page)
* `<section>` – a thematic grouping of content
* `<article>` – an independent, self-contained piece of content (e.g., a blog post)
* `<aside>` – secondary content related to the main content (e.g., a sidebar)
* `<footer>` – bottom section of a page or section, often contains contact info, copyright

### **Text content**

* `<h1>`…`<h6>` – headings with a defined hierarchy
* `<p>` – paragraph of text
* `<blockquote>` – long quotation
* `<cite>` – citation source
* `<abbr>` – abbreviation or acronym
* `<time>` – specific time or date

### **Media & description**

* `<figure>` – self-contained media (image, chart, code block)
* `<figcaption>` – caption or description for `<figure>`
* `<mark>` – highlighted or marked text
* `<address>` – contact information

</details>

**4.What’s the difference between `<div>`and `<section>`?**
<details>
  
  <summary>Answer:</summary>

  The key difference between `<div>` and `<section>` is **semantics** — what the tag *means* in the context of the page.

### **1. `<div>`**

* **Meaning:** No semantic meaning — just a generic container.
* **Purpose:** Groups content purely for styling or scripting.
* **When to use:** When there is no more meaningful semantic tag for that content.
* **Example:**

```html
<div class="card">
  <h3>Title</h3>
  <p>Some content here...</p>
</div>
```

### **2. `<section>`**

* **Meaning:** A *thematic* grouping of related content.
* **Purpose:** Divides the document into logical sections that should have a heading.
* **When to use:** When the content within can be described as a distinct “section” of a document.
* **Example:**

```html
<section>
  <h2>News</h2>
  <p>Latest updates from our company...</p>
</section>
```

### **3. Main differences:**

| Feature             | `<div>`                 | `<section>`                               |
| ------------------- | ----------------------- | ----------------------------------------- |
| Semantic meaning    | ❌ None                  | ✅ Yes — thematic grouping                 |
| Accessibility       | Not announced specially | Recognized as a section by screen readers |
| Heading requirement | Not required            | Recommended to have a heading inside      |
| SEO impact          | Neutral                 | Can improve structure for search engines  |

💡 **Rule of thumb:**

* Use `<section>` when the content has a **logical, standalone topic** and could appear in a document outline.
* Use `<div>` for **purely structural or styling purposes**.

</details>


**5.What is DOCTYPE and why is it needed?**

<details>

  
  <summary>Answer:</summary>

**`<!DOCTYPE>`** is a declaration that tells the browser **which HTML version and rules** it should use to interpret the page.

### **1. What it does**

* It’s **not** an HTML tag — it’s an instruction to the browser.
* Without it, browsers may switch to **quirks mode**, where they try to mimic very old, non-standard browser behavior (hello, early 2000s! 👋).
* With it, browsers use **standards mode**, following modern HTML/CSS rules.

### **2. Modern HTML DOCTYPE**

In HTML5, the declaration is simple:

```html
<!DOCTYPE html>
```

* This tells the browser: *“Use HTML5 rules and standards mode.”*

### **3. Why it’s needed**

1. **Consistency:** Ensures the page renders the same way in different browsers.
2. **Compatibility:** Prevents old rendering quirks from breaking your layout.
3. **SEO & accessibility:** Standards mode improves semantic interpretation.

### **4. Example**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Page</title>
</head>
<body>
  <h1>Hello World!</h1>
</body>
</html>
```

💡 **Interview tip:**  *“What happens if you omit DOCTYPE?”*, answer:

* The browser may enter **quirks mode** and ignore some modern CSS/HTML rules, leading to layout issues.
  

</details>

**6.What are block-level and inline elements? Examples.**

<details>
  
  <summary>Answer:</summary>


**Block-level** and **inline** elements are two main categories of HTML elements that differ in how they behave in the page layout.

## **1. Block-level elements**

**Definition:**

* Always start on a **new line**.
* Expand to fill the **full width** of their parent container by default.
* Can contain **other block-level and inline** elements.
* Respect `width`, `height`, `margin`, and `padding` in all directions.

**Examples:**

```html
<div>...</div>
<section>...</section>
<article>...</article>
<header>...</header>
<footer>...</footer>
<h1>...</h1> <!-- also h2–h6 -->
<p>...</p>
<ul>...</ul>
<li>...</li>
```

## **2. Inline elements**

**Definition:**

* Do **not** start on a new line — they flow **within text**.
* Occupy only as much width as their content.
* Can contain **only other inline elements or text** (generally).
* `width` and `height` **do not** apply directly (only horizontal padding/margins work fully).

**Examples:**

```html
<span>...</span>
<a href="#">...</a>
<strong>...</strong>
<em>...</em>
<img src="..." alt="">
<abbr>...</abbr>
<code>...</code>
```

## **3. Key differences table**

| Feature                     | Block-level | Inline               |
| --------------------------- | ----------- | -------------------- |
| Starts on new line?         | ✅ Yes       | ❌ No                 |
| Takes full width?           | ✅ Yes       | ❌ Only content width |
| Can contain block elements? | ✅ Yes       | ❌ Usually no         |
| Can set `width`/`height`?   | ✅ Yes       | ❌ Limited            |


💡 **Extra note:** There are also **inline-block** elements (e.g., `display: inline-block`), which behave like inline elements but can have width/height set.

</details>

**7.What is the basic structure of an HTML document?**

<details>
  
  <summary>Answer:</summary>


The **basic structure of an HTML document** defines the minimal setup that browsers need to correctly interpret and render a webpage.


## **HTML5 basic structure**

```html
<!DOCTYPE html> <!-- 1. Doctype declaration -->
<html lang="en"> <!-- 2. Root element -->

<head> <!-- 3. Head section (metadata) -->
  <meta charset="UTF-8"> <!-- Character encoding -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Responsive scaling -->
  <title>Page Title</title> <!-- Title shown in browser tab -->
</head>

<body> <!-- 4. Body section (visible content) -->
  <h1>Hello World</h1>
  <p>This is a basic HTML page.</p>
</body>

</html>
```

## **Breakdown of parts**

1. **`<!DOCTYPE html>`** → Tells the browser to use HTML5 in standards mode.
2. **`<html>`** → The root element containing all HTML content.

   * `lang="en"` helps accessibility and SEO by specifying the language.
3. **`<head>`** → Contains **metadata**, not shown directly on the page (title, meta tags, CSS links, scripts).
4. **`<body>`** → Contains all the visible content: text, images, links, forms, etc.

💡 **Interview tip:**
 *“Is `<!DOCTYPE>` an HTML tag?”* — the answer is **no**; it’s a declaration, not a tag.


</details>

📌 Forms and Input

**8.What types of <input> are there?**

<details>
  
  <summary>Answer:</summary>

The `<input>` element has many **types**, each changing how the browser displays it and how it handles user input.

## **1. Basic text inputs**

| Type       | Description                                       | Example                   |
| ---------- | ------------------------------------------------- | ------------------------- |
| `text`     | Single-line plain text                            | `<input type="text">`     |
| `password` | Text hidden with dots/asterisks                   | `<input type="password">` |
| `email`    | Validates email format                            | `<input type="email">`    |
| `url`      | Validates URL format                              | `<input type="url">`      |
| `search`   | Search field with clear button (in some browsers) | `<input type="search">`   |
| `tel`      | Phone number (may open numeric keypad on mobile)  | `<input type="tel">`      |


## **2. Numeric inputs**

| Type     | Description                       | Example                                  |
| -------- | --------------------------------- | ---------------------------------------- |
| `number` | Numeric value with up/down arrows | `<input type="number">`                  |
| `range`  | Slider control                    | `<input type="range" min="0" max="100">` |

## **3. Date & time inputs**

| Type             | Description              | Example                         |
| ---------------- | ------------------------ | ------------------------------- |
| `date`           | Date picker (YYYY-MM-DD) | `<input type="date">`           |
| `time`           | Time picker (HH\:MM)     | `<input type="time">`           |
| `datetime-local` | Local date + time picker | `<input type="datetime-local">` |
| `month`          | Month/year picker        | `<input type="month">`          |
| `week`           | Week/year picker         | `<input type="week">`           |

## **4. Choice inputs**

| Type       | Description                 | Example                              |
| ---------- | --------------------------- | ------------------------------------ |
| `checkbox` | Multiple selectable options | `<input type="checkbox">`            |
| `radio`    | Single choice in a group    | `<input type="radio" name="option">` |
| `color`    | Color picker                | `<input type="color">`               |

## **5. File & buttons**

| Type     | Description              | Example                                  |
| -------- | ------------------------ | ---------------------------------------- |
| `file`   | File upload field        | `<input type="file">`                    |
| `submit` | Submits the form         | `<input type="submit" value="Send">`     |
| `reset`  | Resets the form fields   | `<input type="reset">`                   |
| `button` | Generic clickable button | `<input type="button" value="Click me">` |
| `image`  | Image as a submit button | `<input type="image" src="btn.png">`     |

💡 **Interview tip:**

* Always pair inputs with a `<label>` for accessibility.
* Not all input types look the same across browsers — test in multiple environments.

</details>

**9.What is a label and how is it connected to an input?**

<details>
  
  <summary>Answer:</summary>


  A **`<label>`** in HTML is a semantic element that defines a caption or description for a form control (like an `<input>`, `<textarea>`, `<select>`).

Its main purposes are:

* **Accessibility** — screen readers can announce the label for the input.
* **Better UX** — clicking the label focuses or activates the related input.

## **1. Ways to connect `<label>` to `<input>`**

### **Option 1: Using the `for` attribute**

* The `for` value must match the input’s `id`.

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

✅ Clicking "Email:" focuses the input.

### **Option 2: Wrapping the input inside the label**

```html
<label>
  Email:
  <input type="email" name="email">
</label>
```

✅ No `for` or `id` needed — the label is automatically linked.

## **2. Why it matters**

* Improves **accessibility** for visually impaired users.
* Expands clickable area (good for checkboxes/radios).
* Helps browsers associate input values with their descriptions.

💡 **Interview tip:**
 *“What happens if you don’t use a `<label>`?”*, answer:

* Users can still type, but accessibility and usability suffer — especially for small controls like checkboxes.


</details>

**10.What is the name attribute and why is it important in forms?**

<details>
  
  <summary>Answer:</summary>

  The **`name`** attribute in form elements is used to **identify the data** when the form is submitted.

## **1. What it does**

* Each form control (`<input>`, `<textarea>`, `<select>`, etc.) can have a `name`.
* When the form is submitted, the browser sends data as **name=value** pairs to the server.
* Without a `name`, the input’s value will **not be sent** in the form submission.

## **2. Example**

```html
<form action="/submit" method="post">
  <input type="text" name="username" value="John">
  <input type="password" name="password" value="12345">
  <input type="submit" value="Send">
</form>
```

When submitted, the server receives:

```
username=John&password=12345
```

## **3. Why it’s important**

1. **Server communication** → The backend identifies which field is which.
2. **Form binding** → JavaScript and frameworks use `name` for data binding and validation.
3. **Accessibility & consistency** → Makes data handling predictable.

💡 **Interview tip:**

* If you forget the `name` attribute, that field’s value will **not** be sent at all.
* `id` is for *label association and JS targeting*, but `name` is for *form data submission*.


</details>

📌 Attributes

**11.What does the alt attribute do for an image?**

<details>
  
  <summary>Answer:</summary>

  The **`alt`** attribute (alternative text) in an `<img>` tag provides a **text description of the image**.

## **1. Main purposes**

1. **Accessibility** → Screen readers read the `alt` text aloud for visually impaired users.
2. **Fallback content** → If the image can’t load, the `alt` text is shown instead.
3. **SEO** → Search engines use it to understand the image content.

## **2. Example**

```html
<img src="cat.jpg" alt="A black cat sitting on a windowsill">
```

* If the image loads → The user sees the picture.
* If the image fails → The user sees *A black cat sitting on a windowsill*.
* Screen readers will announce: *“Image: A black cat sitting on a windowsill”*.

## **3. Special cases**

* **Decorative images** → Use an **empty `alt`** (`alt=""`) so screen readers skip it:

```html
<img src="border.png" alt="">
```

* **Don’t repeat “image of…”** → Screen readers already announce it’s an image.

💡 **Interview tip:** If they ask *“What happens if you omit `alt`?”*:

* Accessibility suffers — screen readers may read the file name (e.g., *cat.jpg*), which is not helpful.
* SEO for images is worse.

</details>

**12.What’s the difference between id and class?**

<details>
  
  <summary>Answer:</summary>


  The **difference between `id` and `class`** comes down to **uniqueness** and **intended use**.

## **1. `id`**

* **Unique** → Should be used **only once per page**.
* Used to **identify a single element**.
* Often used for:

  * JavaScript targeting (`document.getElementById`)
  * Linking to anchors (`<a href="#section1">`)
  * Accessibility associations (`<label for="email">`)

**Example:**

```html
<div id="header">Main header</div>
```

## **2. `class`**

* **Reusable** → Can be applied to **multiple elements**.
* Used to **group elements** for styling or scripting.
* Often used for:

  * Applying CSS styles
  * Selecting multiple elements in JavaScript (`document.querySelectorAll('.card')`)

**Example:**

```html
<div class="card">Product 1</div>
<div class="card">Product 2</div>
```

## **3. Comparison table**

| Feature           | `id`                      | `class`                                          |
| ----------------- | ------------------------- | ------------------------------------------------ |
| Uniqueness        | ✅ Yes, only once per page | ❌ No, can repeat                                 |
| CSS specificity   | Higher                    | Lower                                            |
| JavaScript access | `getElementById()`        | `getElementsByClassName()`, `querySelectorAll()` |
| Main use          | Identify one element      | Group multiple elements                          |

💡 **Interview tip:**

* *“Can you style an element with an `id` in CSS?”* → Yes, use `#idName {}`.
* But prefer **classes** for styling, and `id` for unique identification.

</details>

**13.What is the data- attribute used for?**

<details>
  
  <summary>Answer:</summary>

  The **`data-*` attribute** is used to store **custom data** inside HTML elements without affecting their rendering.

## **1. How it works**

* Any attribute that starts with `data-` is valid (e.g., `data-user-id`, `data-role`).
* The data is **invisible** to the user but accessible via:

  * **JavaScript** (`element.dataset`)
  * **CSS attribute selectors** (`[data-role="admin"]`)

## **2. Example**

```html
<button data-user-id="42" data-role="admin">
  Edit User
</button>

<script>
  const btn = document.querySelector('button');
  console.log(btn.dataset.userId); // "42"
  console.log(btn.dataset.role);   // "admin"
</script>
```

## **3. Common uses**

1. Storing **IDs, states, or settings** for JS scripts.
2. Passing extra info without making extra server requests.
3. Marking elements for **dynamic behavior** (e.g., modals, tooltips).

## **4. Best practices**

* Use **lowercase** and **hyphen-separated** names: `data-user-id`, `data-theme-color`.
* Don’t store **sensitive data** (users can see it in HTML).
* Avoid replacing JSON APIs with huge `data-*` blobs — keep it light.

💡 **Interview tip:**“Why not just use a class or id?”* →
Because `data-*` is **meant for storing extra information**, while `class`/`id` is for styling and identifying elements.


</details>

**What are aria-* attributes and why are they important? (Accessibility)**

📌 Scripts and Links

**14.What is the difference between <script>, <noscript>, defer, and async?**

<details>
  
  <summary>Answer:</summary>

  Here’s the breakdown of the difference between **`<script>`**, `defer`, and `async` in HTML:

## **1. `<script>` (default behavior)**

```html
<script src="script.js"></script>
```

* **How it loads:** Browser **downloads** the script immediately, **blocks HTML parsing**, then **executes** it before continuing.
* **When to use:** For small scripts or ones that must run **before** rendering continues (e.g., critical inline scripts).
* **Drawback:** Slows down page loading because parsing stops until the script finishes.

## **2. `defer` attribute**

```html
<script src="script.js" defer></script>
```

* **How it loads:**

  1. Downloads **in parallel** with HTML parsing.
  2. Executes **after** HTML is fully parsed (before `DOMContentLoaded`).
* **Order:** Deferred scripts execute **in the order they appear** in the HTML.
* **When to use:** For scripts that need access to the full DOM (e.g., DOM manipulation).

## **3. `async` attribute**

```html
<script src="script.js" async></script>
```

* **How it loads:**

  1. Downloads **in parallel** with HTML parsing.
  2. Executes **immediately after downloading**, possibly **before** HTML parsing is done.
* **Order:** **Not guaranteed** — scripts may run in any order.
* **When to use:** For independent scripts (e.g., analytics, ads) that don’t depend on DOM or other scripts.

## **4. Summary table**

| Attribute | Download    | Execution          | Blocks HTML parsing? | Keeps script order? | Best for                  |
| --------- | ----------- | ------------------ | -------------------- | ------------------- | ------------------------- |
| *(none)*  | Immediately | Immediately        | ✅ Yes                | ✅ Yes               | Critical blocking scripts |
| `defer`   | Parallel    | After HTML parsing | ❌ No                 | ✅ Yes               | DOM-dependent scripts     |
| `async`   | Parallel    | As soon as ready   | ❌ No                 | ❌ No                | Independent scripts       |

💡 **Interview tip:**
 *“Which is better, `defer` or `async`?”* →

* Use **`defer`** for most scripts that interact with the DOM.
* Use **`async`** for scripts that don’t depend on page content or other scripts.

</details>

**15.What does rel="noopener noreferrer" do in links?**

<details>
  
  <summary>Answer:</summary>

  The attribute **`rel="noopener noreferrer"`** is used in `<a>` tags (usually with `target="_blank"`) for **security** and **privacy**.

## **1. Why it’s needed**

When you use:

```html
<a href="https://example.com" target="_blank">Visit</a>
```

* The new page can access `window.opener` and **control the original page** (e.g., change location, run malicious code).
* Also, by default, the **HTTP referrer** (the URL of your page) is sent to the new page.

## **2. What each part does**

### **`noopener`**

* Prevents the opened page from accessing `window.opener`.
* Stops potential **tabnabbing** attacks (where the new page changes your original page to a phishing site).

### **`noreferrer`**

* Prevents the browser from sending the **HTTP referrer header**.
* Hides your page’s URL from the site you’re linking to.
* Also implicitly includes `noopener` in most browsers.

## **3. Example**

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  Safe External Link
</a>
```

## **4. Best practice**

* Always add `rel="noopener noreferrer"` to **external links** with `target="_blank"`.
* For internal links (same domain), `noopener` alone is usually enough.

💡 **Interview tip:**
 *“Is `noreferrer` always needed if you have `noopener`?”* →
No, but `noreferrer` adds privacy by hiding your page’s URL. It’s extra protection.


</details>
