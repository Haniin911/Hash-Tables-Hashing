🧵 Chaining vs Probing: These Concepts are used for "Handling Collisions"

Let’s say two food items for example (Fish and Rice) both end up on page 3 using your hash function. This is a collision.
How do we handle it?

There are two popular ways: Chaining and Probing.

🧶 1. Chaining (Separate Chaining)
Think of it like this:

📖 Page 3 becomes a list of items, not just a single price.
You go to page 3.

Instead of finding only one food item, you find a mini list of all food items that ended up there.
For example:
Page 3:
- Fish → $20
- Rice → $9
- Fries → $15
💡 When you search for the price of Rice, you just scan this small list on the page.
✅ Pros:
Easy to implement.
The table can still store more than one item per slot.
❌ Cons:
If too many items land on the same page, the list gets long → slower.

🔁 2. Probing (Open Addressing)
In probing, each page can hold only one item. So if page 3 is already full, you try to find the next empty page using a pattern.
For example:
Fish → goes to page 3.
Rice → tries page 3, finds it full, so tries page 4.
If page 4 is full too, try page 5, and so on…
This process is called linear probing.
There are other variations too, like quadratic probing or double hashing, where you jump in different ways.

✅ Pros:
No need for extra memory for lists.
Can be memory-efficient for small datasets.
❌ Cons:
More sensitive to load factor — when the table gets full, it becomes much slower.
Needs careful handling to avoid infinite loops or clustering.
