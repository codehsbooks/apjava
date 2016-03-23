# What is an Algorithm?

An algorithm is a set of steps to follow to solve a particular problem. Programs can perform specific tasks by following the steps of an algorithm.

## Following a Recipe
Algorithms are like recipes in cooking. By following the steps of the recipe, you can create the desired food. Here's a sample recipe for chocoloate chip cookies, adapted from a [common cookie recipe](http://allrecipes.com/recipe/10813/best-chocolate-chip-cookies/):

1. Preheat the oven to 350 degrees Fahrenheit.
2. In a mixing bowl, mix the following ingredients together until smooth:
    - 1 cup butter
    - 1 cup white sugar
    - 1 cup brown sugar
3. Beat in 2 eggs, one at a time.
4. Stir in 2 teaspoons vanilla extract.
5. Dissolve 1 teaspoon baking soda in hot water and add to mixture.
6. Stir in the following ingredients:
    - 1/2 teaspoon salt
    - 3 cups flour
    - 2 cups chocolate chips
7. When mixed thoroughly, drop cookie dough onto baking sheet.
8. Bake at 350 degrees Fahrenheit for 10 minutes.

To make delicious cookies, you'll need to follow the steps in the correct order and with the correct ingredients. What would happen if you used twice as much flour? Or if you put the cookie dough onto the baking sheet before you mixed it together? Your cookies would most likely not turn out very well. That's why it is important to follow the steps from start to finish.

## Programs as Recipes
Computer programs, like recipes, are designed to accomplish specific tasks. Though a program may not be baking cookies, it too must follow a specific set of instructions in order to achieve the desired results.

Though the cookie recipe above is popular, it is certainly not the only chocoloate chip cookie recipe available. Similarly, there are often many different ways to write a program to solve a particular problem. Here is a very simplified example of writing a few different methods that find the average of two numbers:

    public double findAverageA(int a, int b)
    {
        return (double) (a + b) / 2;
    }
    
    public double findAverageB(int a, int b)
    {
        return (a + b) / 2.0;
    }
    
    public double findAverageC(int a, int b)
    {
        int sum = a + b;
        int numerator = sum;
        int denominator = 2;
        double average = (double) numerator / (double) denominator;
        
        average = 15 + average - 15 + 10 - 5 - 3 - 2;
        
        return average;
    }

Each of these programs returns the same result:

    System.out.println(findAverageA(3, 4));
    System.out.println(findAverageB(3, 4));
    System.out.println(findAverageC(3, 4));
    
will print out:

    3.5
    3.5
    3.5
    
Though the results are the same, there are some important differences. And take a look at the `findAverageC` method. It finds the correct solution, but it's doing way more work than the other algorithms! As the programs you write solve bigger and bigger problems, it becomes more important to compare the speed and efficiency of different algorithms. 
