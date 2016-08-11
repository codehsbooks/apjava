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

## Implementing Linear Search

Linear search isn't too difficult to implement. To programmatically searching our list of raffle ticket numbers, we just need to iterate through the list one number at a time. At each new number, if the number matches the desired number, we know that the desirred number is in the list, so we can stop searching and return the index position of the number. If we make it all the way to the end of the list and haven't spotted our desired number, then that means it's not in the list.

Here's what it looks like in pseudocode:

    for every index in the list:
        get the current number at that index position
        if the current number matches our target number:
            return the index
    return not found

We can then turn that pseudocode into real Java code:

    /**
     * This method takes an array called array and a 
     * key to search for, and returns the index of
     * key if it is in the array or -1 if it is not
     * found.
     */
    public int linearSearch(int[] array, int key)
    {
        for(int i = 0; i < array.length; i++)
        {
            int element = array[i];
            if(element == key)
            {
                return i;
            }
        }
        return -1;
    }
        


