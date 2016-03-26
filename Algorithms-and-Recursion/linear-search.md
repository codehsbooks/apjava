# Linear Search

Searching for items in an array is an important and common task in computer science. For example, a meterologist may want to konw the hottest day on record in a fiven month. Teachers may want to find a particular student in a class roster. A skateboard shop may want to check their inventory to see if they have a certain deck in stock. Storing data in a computer allows information like this to be easily searched and retrieved.

## Introducing Linear Search

One way to search through a list of items is to start at the beginning of the list and continue through the list until the desired item is found. If the desired item is not found, then that means it is not in the list.

Suppose that you are given a set of raffle tickets at a school raffle. Each ticket has its own number on it. Your tickets may look like this:

| Ticket | 0 | 1 | 2 | 3 | 4 | 5 |
| ---    |---|---|---|---|---|---|
| Number | 44| 53| 12| 51| 64| 15|

The 0th ticket has number 144, and the ticket at index 4 has raffle number 64. The school will randomly select a number between 1 and 100. If you have the ticket with that number, you win!

What if the school picks 51 as the winning number? As a human, it's easy to look over the whole list and see that you have the ticket with 51 on it. But computers can't look over a whole list the way a human can. Computers need a more programmatic approach to looking through the list.
