# Creating lists

Lists are the way that makes a short piece of information easy to understand. There are tree types of lists i.e. **unordered lists**, **ordered lists**, and **description lists**.

##A. Unordered lists

In unordered list the order of the items doesn't matter . To create a unordered list by HTML we have to use two tags <ul> and <li> .The <ul> tag represents the whole list and <li> tag represents the items of the list . Both <ul> and <li> are the block-level elements. By default there exists a vertical margin and left padding on <ul> element and all the list item(<li>) precede with a bullet point(or solid dot).

```
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ul>
```

##B. Ordered list

This list is similar with the unordered list but the order of the items matters. In HTML ordered list represents by <ol> tag and the items represents by <li>. The sequence of the items in which it will represented is really important. Therefore, instead of bullet points the marker of each item will be a number in an ordered list. By default an ordered list will begin from 1. However you can set a custom begining point or reversed the order of the item, using start and reversed attribute.

```
<ol>
  <li>Milk</li>
  <li>Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ol>
```

>>Ordered list has some attributes which can change the marker of the items.

###(i) Start Attribute

he start attribute on <ol> element will decide from which the ordered list should start.

```
<ol start="20">
  <li>Milk</li>
  <li>Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ol>
```

In the above example list marker will start from 20 i.e. milk will have the marker of 20 and next item will have the marker of 21 .

###(ii) Reversed Attribute

The reversed is a boolean attribute, that reverse the order of items inside ordered lists. By default the value for reversed attribute is false, just adding reversed without any value it becomes true.

```
<ol reversed>
  <li>Milk</li>
  <li>Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ol>
```
In the above example order of the items will start from 4 to 1.

###(iii) Value Attribute

This property is used for give a specific order to an item individually .

```
<ol>
  <li>Milk</li>
  <li value="10">Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ol>
```
In this example list will begin at 1 and the second item marker will be 10 and afterwards each items will be having upwards value from 10 i.e (11,12,13 etc.).

>Nesting Lists
>
One list can have another list inside it i.e. (sub list).
```
<ol>
  <li>Milk</li>
  <li>Bread</li>
  <li>
    Fruits
    <ul>
      <li>Apple</li>
      <li>Banana</li>
      <li>Mango</li>
    </ul>
  </li>
  <li>Tea</li>
</ol>
```

> CSS has handful of styling properties to style list items markers .

###(i) List Style Type Property

The list-style-type property is used to set the content of a list item marker. We can make the marker a square by using "square" value of the list-style-type property.

```
<ul>
  <li>Milk</li>
  <li>Bread</li>
  <li>Tea</li>
  <li>Fruits</li>
</ul>
```
```
ul {
  list-style-type: square;
}
```
Other acceptable values of list-style-type property :

| list style type value     |        content                          |
| ------------------------- | --------------------------------------- |
| disc                      | A filled circle                         |
| circle                    | A hollow circle                         |
| square                    | A filled square                         |
| decimal                   | Decimal numbers                         |
| decimal-leading-zero      | Decimal numbers padded by initial zeros |
| lower-roman               | Lowercase roman numerals                |
| upper-roman               | Uppercase roman numerals                |
| lower-greek               | Lowercase classical Greek               |
| lower-alpha / lower-latin	| Lowercase ASCII letters                 |
| upper-alpha / upper-latin | Uppercase ASCII letters                 |
| armenian                  | Traditional Armenian numbering          |
| georgian                  | Traditional Georgian numbering          |
| none                      | No list item                            |


###(ii) List Style Position Property

This property is used to positioning list item marker. The list-style-position property accepts three values "outside",
"inside" and "inherit". The "outside" value keeps the marker on the left side and outside of the content and allow content to wrap below the marker . The inside value will keep the marker wihin the content on the left side, where the content can wrap below the marker.

```
ul {
  list-style-postion: inside;
}
```

###  Shorthand List Style Property

The list-style is the shorthand property for list-style-type, list-style-position and listi-style-image.

```
ul {
  list-style: square outside none;
}
```

## C. Description Lists

Description lists is not used unlike the unordered list and ordered list . To accomplish description list in HTML, <dl> tag is used. The <dl> element requires two block-level element, <dt> and <dd>. The <dt> represetns the description term and <dd> reprsents the description of the term. Similar to the <ol> and <ul>, <dl> element include vertical margins and <dd> element includes left margin.

```
<dl>
  <dt>study</dt>
  <dd>
    The devotion of time and attention to acquiring knowledge on an academic
    subject, especially by means of books
  </dd>
  <dt>design</dt>
  <dd>
    A plan or drawing produced to show the look and function or workings of a
    building, garment, or other object before it is built or made
  </dd>
  <dd>
    Purpose, planning, or intention that exists or is thought to exist behind an
    action, fact, or material object
  </dd>
  <dt>business</dt>
  <dt>work</dt>
  <dd>A person's regular occupation, profession, or trade</dd>
</dl>
```
