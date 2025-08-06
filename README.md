🔷 HTML

📌 Basics

**1.What is HTML and what is it used for?**

<details>
  <summary>Answer:</summary>
  
&nbsp;&nbsp;&nbsp;&nbsp;HTML stands for HyperText Markup Language. It is the standard language used to create and structure content on the web.

&nbsp;&nbsp;&nbsp;&nbsp;HTML is used to:

&nbsp;&nbsp;&nbsp;&nbsp;Structure content on a webpage — like paragraphs, headings, images, lists, tables, forms, and links.

&nbsp;&nbsp;&nbsp;&nbsp;Define the meaning of elements — for example:

&nbsp;&nbsp;&nbsp;&nbsp;`<h1>` to `<h6>`: headings

&nbsp;&nbsp;&nbsp;&nbsp;`<p>`: paragraph

&nbsp;&nbsp;&nbsp;&nbsp;`<img>`: image

&nbsp;&nbsp;&nbsp;&nbsp;`<a>`: hyperlink

&nbsp;&nbsp;&nbsp;&nbsp;Embed media like images, videos, and audio.

&nbsp;&nbsp;&nbsp;&nbsp;Create interactive forms for user input.

&nbsp;&nbsp;&nbsp;&nbsp;Provide semantic meaning for search engines and assistive technologies (e.g., screen readers).

&nbsp;&nbsp;&nbsp;&nbsp;HTML is not a programming language.

&nbsp;&nbsp;&nbsp;&nbsp;It's a markup language that tells browsers how to display content.
  
</details> 
   



**2.What is semantic HTML? Give examples.**

<details>
  <summary>Answer:</summary>

&nbsp;&nbsp;&nbsp;&nbsp;Semantic HTML uses tags that describe the purpose of the content inside them, rather than just how it looks.

&nbsp;&nbsp;&nbsp;&nbsp;For example: `<article>`, `<footer>`, `<header>` — these elements tell you what the content is, not just how to display it.

&nbsp;&nbsp;&nbsp;&nbsp;Why use Semantic HTML?

&nbsp;&nbsp;&nbsp;&nbsp;✅ Better for accessibility (screen readers understand content better).

&nbsp;&nbsp;&nbsp;&nbsp;✅ Helps with SEO (search engines understand page structure).

&nbsp;&nbsp;&nbsp;&nbsp;✅ Makes your code more readable and organized.

&nbsp;&nbsp;&nbsp;&nbsp;🧱 Examples of Semantic Tags:

Tag	Meaning / Use Case
```html

<header>	Top section of a page or section (logo, nav, intro)
<nav>	     Navigation links
<main>	   Main content of the page
<section>	A distinct section of content
<article>	 A self-contained piece of content (e.g., blog post)
<aside>	 Side content (ads, tips, related links)
<footer>	Footer (copyright, links, contact info)
<figure>  Media content with a caption
<figcaption>	 Caption for a figure
<mark>	Highlighted or important text
<time>	Machine-readable time/date

```
  
🧾 Semantic HTML Example:

  
```html
<article>
  <header>
    <h1>What is Semantic HTML?</h1>
    <p><time datetime="2025-08-06">August 6, 2025</time> by Jane Doe</p>
  </header>

  <section>
    <h2>Definition</h2>
    <p>Semantic HTML tags describe the meaning of the content...</p>
  </section>

  <aside>
    <p>Did you know? Semantic tags improve accessibility.</p>
  </aside>

  <footer>
    <p>Published by WebDev Academy</p>
  </footer>
</article>
```

❌ Non-semantic alternative:

```html
<div class="header">...</div>
   <div class="nav">...</div>
   <div class="content">...</div>
```
</details>

**3.What semantic tags do you know?**

**4.What’s the difference between `<div>`and `<section>`?**

**5.What is DOCTYPE and why is it needed?**

**6.What are block-level and inline elements? Examples.**

**7.What is the basic structure of an HTML document?**

📌 Forms and Input

**8.What types of <input> are there?**

**9.What is a label and how is it connected to an input?**

**10.What is the name attribute and why is it important in forms?**

📌 Attributes

**11.What does the alt attribute do for an image?**

**12.What’s the difference between id and class?**

**13.What is the data- attribute used for?**

**What are aria-* attributes and why are they important? (Accessibility)**

📌 Scripts and Links

**14.What is the difference between <script>, <noscript>, defer, and async?**

**15.What does rel="noopener noreferrer" do in links?**
