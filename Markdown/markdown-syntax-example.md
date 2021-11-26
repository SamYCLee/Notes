# Markdown Syntax Example

This note is a collection of markdown syntax, including both [basic][1] and [extended][2] ones.

## Basic Syntax

----

### **Heading**

#### *Level 1* (The upmost level)

    # Heading

> There is an alternative syntax for level 1 heading

    Heading
    ===

#### *Level 2*

    ## Heading

> There is an alternative syntax for level 1 heading

    Heading
    ---

#### *Level 3*

    ### Heading

#### *Level 4*

    #### Heading

#### *Level 5*

    ##### Heading

#### *Level 6*

    ###### Heading

### **Bold**

    **Bold**

### **Italic**

    *Italic*

### **Bold and Italic**

    ***Bold and Italic***

### **Blockquotes**

#### *Single line*

    > Quote

#### *Multiple line*

    > Quote 1
    > Quote 2
    > Quote 3

#### *Nested*

    > Quote Layer 1
    >> Quote Layer 2
    >>> Quote Layer 3

### **Lists**

#### *Ordered Lists*

    1. First Item
    2. Second Item
    3. Third Item
       1. Alpha
       2. Beta
    4. Forth Item

#### *Unordered Lists*

    - First Item
    - Second Item
    - Third Item

OR

    * First Item
    * Second Item
    * Third Item

OR

    + First Item
    + Second Item
    + Third Item

### **Code Block**

> Code blocks are normally indented four spaces or one tab. When they’re in a list, indent them eight spaces or two tabs.

----

## Extended Syntax

Not all Markdown applications support extended syntax elements. You’ll need to check whether or not the lightweight markup language your application is using supports the extended syntax elements you want to use. If it doesn’t, it may still be possible to enable extensions in your Markdown processor. (Quote: [Reference][2])

----

### **Table**

    | Header | Description |
    | --- | --- |
    | Header 1 | content1 |

#### Alignment in table

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

    | Syntax      | Description | Test Text     |
    | :---        |    :----:   |          ---: |
    | Header      | Title       | Here's this   |
    | Paragraph   | Text        | And more      |


[1]: https://www.markdownguide.org/basic-syntax/
[2]: https://www.markdownguide.org/extended-syntax/