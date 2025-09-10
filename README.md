# 🔎 XPath Cheat Sheet for Test Automation

A handy reference for **Selenium, Playwright, Cypress, or any automation tool** that uses XPath.  
Covers **basic → advanced locator strategies** with examples and use cases.

---

## 📌 XPath Types and Examples

| **XPath Type** | **Example** | **Use Case / Explanation** |
|----------------|-------------|-----------------------------|
| **Absolute XPath** | `/html/body/div/div[2]/input` | Selects element from root (`/`). Brittle (breaks if structure changes). |
| **Relative XPath** | `//div/input` | Starts from anywhere in DOM (`//`). More stable than absolute. |
| **By Tag Name** | `//input` | Finds all `<input>` elements on page. |
| **By Attribute** | `//input[@id='username']` | Selects element by specific attribute value. |
| **Multiple Attributes** | `//input[@type='text' and @name='email']` | Uses `and/or` for precise element matching. |
| **By Text** | `//h1[text()='Welcome']` | Matches element based on exact text. |
| **Contains (Attribute)** | `//input[contains(@id,'user')]` | Finds elements where attribute contains given text. |
| **Contains (Text)** | `//button[contains(text(),'Login')]` | Finds elements where visible text contains value. |
| **Starts-with()** | `//input[starts-with(@id,'user')]` | Selects attributes/text that start with given string. |
| **Ends-with()** *(XPath 2.0 only)* | `//input[ends-with(@id,'name')]` | Matches attributes/text ending with given value (not always supported). |
| **Indexing** | `(//button[@class='btn'])[2]` | Selects the 2nd matching element. |
| **First Element** | `(//input[@type='text'])[1]` | Selects the first element from a group. |
| **Last Element** | `(//input[@type='text'])[last()]` | Selects the last element from a group. |
| **Parent Axis** | `//input[@id='username']/parent::div` | Moves **up** to parent node. |
| **Child Axis** | `//div[@id='container']/child::input` | Finds **direct child** nodes. |
| **Ancestor Axis** | `//input[@id='username']/ancestor::form` | Finds all parent elements up the hierarchy. |
| **Descendant Axis** | `//form[@id='login']/descendant::input` | Selects all nested children (grandchildren, etc.). |
| **Following Axis** | `//label[@for='user']/following::input[1]` | Selects element **after** the current one in DOM. |
| **Preceding Axis** | `//input[@id='password']/preceding::label` | Selects element **before** the current one in DOM. |
| **Following-Sibling** | `//h2/following-sibling::p` | Selects the next element at the same level. |
| **Preceding-Sibling** | `//p[@id='para2']/preceding-sibling::p` | Selects the previous element at the same level. |
| **Wildcard `*`** | `//*[@id='submit']` | Selects any element with given attribute. |
| **Normalize-space()** | `//button[normalize-space(text())='Login']` | Ignores spaces when matching text. |
| **Not()** | `//input[not(@type='hidden')]` | Selects elements that do **not** match the condition. |

---

## ⚡ Advanced XPath Locators

| **Advanced Technique** | **Example** | **Use Case / Explanation** |
|-------------------------|-------------|-----------------------------|
| **Union (`|`)** | `//input[@type='text'] | //textarea` | Selects multiple types of elements at once. |
| **Group Conditions** | `//input[@type='text' and (@id='user' or @name='username')]` | Mix `and/or` conditions for flexibility. |
| **Dynamic Attribute Handling** | `//input[contains(@id, concat('user','name'))]` | Builds attributes dynamically with `concat()`. |
| **Position Filters** | `//tr[position() < 3]` | Selects the first 2 rows of a table. |
| **String Functions** | `//a[substring(@href,1,5)='https']` | Finds links starting with `https`. |
| **Count Function** | `//table[count(.//tr)=5]` | Selects a table having exactly 5 rows. |
| **Boolean Functions** | `//input[@id and @name]` | Selects elements having both `id` and `name`. |
| **Contains + Normalize** | `//*[contains(normalize-space(text()),'Login')]` | Matches text ignoring spaces. |
| **Chained Axes** | `//div[@id='main']/child::ul/child::li[1]/following-sibling::li[2]` | Moves across multiple DOM levels. |
| **Self Axis** | `//input[@id='username']/self::input` | Refers to the current node itself. |
| **Namespace Nodes** *(XML testing)* | `//x:book/x:title` | Used for XML with namespaces. |
| **Wildcard for Attributes** | `//*[@*='submit']` | Selects elements where **any attribute** has value `submit`. |
| **OR Between Tags** | `//h1 | //h2` | Selects both `<h1>` and `<h2>` headers. |
| **Deep Descendant** | `//div[@id='container']//input[@type='checkbox']` | Selects all checkboxes under a container (any depth). |
| **Starts-with + Position** | `(//input[starts-with(@id,'user')])[last()]` | Gets last element with dynamic ID. |

---

## ✅ Usage

- Covers **basic → advanced XPath scenarios** in Selenium / Playwright.  
- Useful for **interviews and real-world automation projects**.  
- Helps with **dynamic elements, complex DOMs, and XML parsing**.  

---
**Download the xpath-advanced-practice.html file and practice**
---
📌 Feel free to **star ⭐ this repo** if you find it helpful!
