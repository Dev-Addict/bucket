# Bucket Markup Language(BML)

**BML** is a language that will help you save data in bml format. The syntax is easy to learn and there is the document
to help you understand the language better.

## Getting Started

in order to get started you need to create a file with format of `.bml`.

the syntax is very easy, and you will get used to it very soon. this is the overall look of every line in **BML**

```
element attribute(value) (value)
```

### Simple Example

now for example imagine we are going to turn the header into a **BML** line.

```
header (Getting started)
```

this line will return this in json format

```
[
  {
    "element": "header",
    "value": "Getting Started"
  }
]
```

now imagine another example where you what to set the color of the header too.

### Example with attribute

```
header color(black) (Getting started)
```

this line will return this in json format

```
[
  {
    "color": "black",
    "element": "header",
    "value": "Getting Started"
  }
]
```

## Data Types

+ Boolean: you can represent boolean value with `True` or `False`
+ Integer: integer with no point number
+ Double: double with pointing numbers
+ Character: you can represent character by using `'{character}'`
+ String: you can represent string by using `"{string}"`
+ Array: you can use arrays by using brackets: `[value1, value2]`

## Multiline Formatting

For easier formatting the file you can easily use multiline feature to make it easier to read. The multiline feature
work with an indent if you want to say the attribute for the value is for the last line you put indent at the start of
the line. for an example look at the line below belonging to a country data.

```
country
  name("Iran")
  iso-code("IR")
  phone(98)
  continent("Asia")
  capital("Tehran")
  currency("IRR")
  languages([
    "FA",
    "TR",
    "KU"
  ])
```

this code will return this in json format

```
[
  {
    "capital": "Tehran",
    "continent": "Asia",
    "currency": "IRR",
    "element": "country",
    "iso-code": "IR",
    "languages": [
      "FA",
      "KU",
      "TR"
    ],
    "name": "Iran",
    "phone": 98
  }
]
```
