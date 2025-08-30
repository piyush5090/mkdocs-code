# Markdown Usage Guide

This section explains in simple terms how to write different things in Markdown. For every example, we show the Markdown code and a preview of how it renders on the page.

## **Chapter 1: The Basics**

### **What is Markdown?**

Markdown is a simple way to write formatted text that gets converted into HTML (the language of web pages). You write in plain text with a few special symbols, and a processor (like MkDocs) turns it into a beautiful web page.

### **Headings

Headings are titles for your document sections. Think of them as outlines. The subheadings (`##`, `###`) are what will appear in the right-side navigation menu.

**Example:**
```markdown
# Main Title
## Section A
### Sub-section A.1
```
**Renders as:**
# Main Title
## Section A
### Sub-section A.1

### Paragraphs & Line Breaks

- To create a new paragraph, leave a blank line between lines of text.
- To force a line break inside a paragraph, end a line with two or more spaces.

---

## **Chapter 2: Text Formatting**

This is how you make text stand out. When the site is built, Markdown converts these symbols into HTML tags (e.g., `**text**` becomes `<strong>text</strong>`).

### **Italic Text**
- **Purpose:** Used for emphasis, titles of works, or foreign words.
- **Syntax:** Wrap text in one asterisk `*` or underscore `_`.

```markdown
The system is *mostly* stable.
```
**Renders as:** The system is *mostly* stable.

### **Bold Text**
- **Purpose:** Used for strong importance or to draw the reader's attention.
- **Syntax:** Wrap text in two asterisks `**` or underscores `__`.

```markdown
**Warning:** Do not delete the configuration file.
```
**Renders as:** **Warning:** Do not delete the configuration file.

### **Strikethrough**
- **Purpose:** Used to show something is no longer relevant.
- **Syntax:** Wrap text in two tildes `~~`.

```markdown
Version 1.0 is ~~no longer supported~~.
```
**Renders as:** Version 1.0 is ~~no longer supported~~.

---

## **Chapter 3: Lists**

### **Unordered Lists (Bullets)**
Used when the order of items does not matter. To nest a list item, indent it with four spaces.

**Example:**
```markdown
Project requirements:
- Fast performance
- Low memory usage
    - Optimize PNG compression (Note the 4-space indent)
- Cross-platform support
```

**Renders as:**
- Fast performance
- Low memory usage
    - Optimize PNG compression (Note the 4-space indent)
- Cross-platform support

### **Ordered Lists (Numbers)**
Used for step-by-step instructions where order is critical.

**Example:**
```markdown
Deployment Instructions:
1. Shut down the old server.
2. Run the migration script.
3. Start the new server.
```

**Renders as:**
1. Shut down the old server.
2. Run the migration script.
3. Start the new server.

### **Task Lists (Checkboxes)**
A special type of list where items can be checked off. Very useful for tracking to-do items.

**Example:**
```markdown
- [x] Write the documentation
- [x] Add the new feature
- [ ] Deploy to production
```
**Renders as:**
- [x] Write the documentation
- [x] Add the new feature
- [ ] Deploy to production

---

## **Chapter 4: Links, Images, and Tables**

### **Links (URLs)**
Links are used to direct the reader to another webpage. You can also add a "title" that appears when a user hovers their mouse over the link.

**Example:**
```markdown
- A simple link: [Visit Google](https://www.google.com)
- A link with a title: [MkDocs Docs](https://www.mkdocs.org/ "Official documentation for MkDocs")
```
**Renders as:**
- A simple link: [Visit Google](https://www.google.com)
- A link with a title: [MkDocs Docs](https://www.mkdocs.org/ "Official documentation for MkDocs")

### **Images**
Images are displayed in your document. The text in the square brackets (`alt text`) is crucial for accessibility, as it describes the image to screen readers.

**Example:**
```markdown
![A diagram of the system architecture](https://www.interviewbit.com/blog/wp-content/uploads/2022/06/System-Architecture-Diagram-1024x645.png)
```
**Renders as:**
![A diagram of the system architecture](https://www.interviewbit.com/blog/wp-content/uploads/2022/06/System-Architecture-Diagram-1024x645.png)

### **Tables**
Tables are useful for organizing data. For complex tables, it is much easier to use an online tool like [Markdown Table Generator](https://www.tablesgenerator.com/markdown_tables).

**Example:**
```markdown
| Command | Description                         |
|:--------|:------------------------------------|
| `mkdocs serve` | Starts the local development server.      |
| `mkdocs build` | Builds the static HTML site.        |
```
**Renders as:**
| Command | Description                         |
|:--------|:------------------------------------|
| `mkdocs serve` | Starts the local development server.      |
| `mkdocs build` | Builds the static HTML site.        |

---

## **Chapter 5: Advanced & Custom Elements**

### **Boxes (Admonitions)**
Admonitions are a special feature of many MkDocs themes that create colored boxes for important information. The syntax is `!!! type "Optional Title"`, and the content must be indented with four spaces.

Below are examples of all common admonition types.

**Note, Info, Summary**
```markdown
!!! note
    This is a note. It's useful for highlighting information.

!!! info "Did you know?"
    This is an info box with a custom title.

!!! summary
    This is a summary or abstract.
```
**Renders as (a styled box):**
> **Note**
> 
> This is a note. It's useful for highlighting information.

> **Did you know?**
> 
> This is an info box with a custom title.

> **Summary**
> 
> This is a summary or abstract.

**Tip, Success, Question**
```markdown
!!! tip
    Try using a keyboard shortcut for faster results.

!!! success "Migration Complete"
    The database migration finished successfully.

!!! question
    What is the difference between `==` and `is` in Python?
```
**Renders as (a styled box):**
> **Tip**
> 
> Try using a keyboard shortcut for faster results.

> **Migration Complete**
> 
> The database migration finished successfully.

> **Question**
> 
> What is the difference between `==` and `is` in Python?

**Warning, Failure, Danger**
```markdown
!!! warning
    This feature is deprecated and will be removed in a future version.

!!! failure
    The build failed with 3 errors.

!!! danger "High-Risk Operation"
    This operation will wipe the database. It cannot be undone.
```
**Renders as (a styled box):**
> **Warning**
> 
> This feature is deprecated and will be removed in a future version.

> **Failure**
> 
> The build failed with 3 errors.

> **Danger**
> 
> This operation will wipe the database. It cannot be undone.

**Bug, Example, Quote**
```markdown
!!! bug
    There is a known issue with rendering on mobile devices.

!!! example
    Here is a working example of the function.

!!! quote "Grace Hopper"
    It's easier to ask forgiveness than it is to get permission.
```
**Renders as (a styled box):**
> **Bug**
> 
> There is a known issue with rendering on mobile devices.

> **Example**
> 
> Here is a working example of the function.

> **Grace Hopper**
> 
> It's easier to ask forgiveness than it is to get permission.

---

### **Using HTML in Markdown**
Because Markdown is converted to HTML, you can use most HTML tags directly in your `.md` files. This is useful for things that Markdown can't do by itself.

#### **Highlighted Text & Colors**
Use the `<mark>` tag to make text look like it was highlighted with a marker. For specific colors, you must use the HTML `<span>` tag with a `style` attribute. **Note: This is not standard Markdown and should be used sparingly.**

**Example:**
```html
Make sure to read the <mark>security section</mark> before deploying.

The status is <span style="color: green;">OK</span>.
However, the legacy system is in a <span style="color: red;">CRITICAL</span> state.
```

**Renders as:**

Make sure to read the <mark>security section</mark> before deploying.
The status is <span style="color: green;">OK</span>.
However, the legacy system is in a <span style="color: red;">CRITICAL</span> state.

#### **Collapsible Sections**
This is perfect for hiding long outputs or supplementary information behind a click.

**Example:**
```html
<details>
<summary>Click to see the full error log</summary>

```
-- Error Log --
Exception in thread "main" java.lang.NullPointerException
    at com.example.myproject.Book.getTitle(Book.java:16)
```

</details>
```

**Renders as:**

<details>
<summary>Click to see the full error log</summary>

```
-- Error Log --
Exception in thread "main" java.lang.NullPointerException
    at com.example.myproject.Book.getTitle(Book.java:16)
```

</details>
