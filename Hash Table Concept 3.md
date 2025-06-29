📊 What is the Load Factor in a Hash Table?
Let’s continue with your restaurant booklet idea.

You have:

A booklet divided into, say, 10 pages (each page is like a slot or index in a hash table).

You're writing food prices on these pages based on the food name → page number using a hash function.

Now…

Let’s say you have written prices for 7 food items in the booklet.

🔍 Load Factor = How Full the Booklet Is
The load factor tells you how full your table (booklet) is.

It’s calculated as:

mathematica
Copy
Edit
Load Factor = Number of Stored Items / Total Number of Pages
In your case:

java
Copy
Edit
Load Factor = 7 / 10 = 0.7
📉 Why Does Load Factor Matter?
A low load factor (like 0.3 or 0.4) means the booklet has plenty of empty pages, so it's less likely two food items end up on the same page (fewer collisions).

A high load factor (like 0.8 or 0.9) means the booklet is getting crowded, and more food items are landing on the same pages (more collisions).

🧠 When Load Factor Gets Too High
Most systems decide:

“If the load factor becomes too high (e.g., above 0.75), let’s resize the table — make a bigger booklet with more pages.”

This is called rehashing:

A new, larger table is created (e.g., 20 pages instead of 10).

All items are rehashed (re-calculated) and placed in their new positions.

