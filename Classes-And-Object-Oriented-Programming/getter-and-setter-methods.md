# Getter and Setter Methods
<hr>
Getter and setter methods allow us to get and set instance variables from the client class. 

We use getter and setter methods for validation, to hide internal representation, expansion, and security. 

### Getter Methods
<hr>
***Getter methods*** allow us to access specific instance variables of an object. ***Getter methods*** are also known as ***accessor methods***.

<br>

##### Creating Getter Methods:
When creating ***getter methods*** there is a common convention you should follow. When naming your ***getter methods*** you should always use this format: `get[Variable Name]` for the name. Some examples of this would be: `getWidth();`, `getHeight()`, and `getColor()`. ***Getter methods*** usually only return the variable we are trying to get. Here are some examples of how this would look:

```Java
private int width = 10;
private int height = 3;
private Color rectCol = Color.blue;

public int getWidth()
{
     return width;
}

public int getHeight()
{
     return height;
}

public Color getColor()
{
    return rectCol;
}
```

### Setter Methods
<hr>
***Setter methods*** allow us to set the values of an object's instance variables. ***Setter methods*** are also known as ***modifier methods***

<br>

##### Creating Setter Methods:
As with ***getter methods*** we use a common convention when creating ***setter methods***. When creating ***setter methods*** you should always use: `set[Variable Name]`. Some common examples include: `setWidth(int width)`, `setHeight(int height)`, `setColor(Color color)`. Here are some examples of how to create these setter methods:


```Java
private int width = 10;
private int height = 3;
private Color rectCol = Color.blue;

public void setWidth(int newWidth)
{
    width = newWidth;
}

public void setHeight(int newHeight)
{
    height = newHeight;
}

public void setColor(Color color)
{
    rectCol = color;
}
```