# ANCAR-MARKDOWN -- RULES

## Headings
Expandable  

Six levels of headings : 1-6  
Follows basic markdown syntax as follows :  

|Syntax|Heading size|
|---|---|
|#|1|
|##|2|
|###...|...|

## Text quick styling
Expandable  
Many stylings  

Default syntax :  
|Syntax|Heading size|
|---|---|
|\~~string~~|~~string~~|
|\*string*|*string*|
|\*\*string**|**string**|
|...|...|

## Tables
Non-expandable

```markdown
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

Set alignment with colons ":"
```markdown
| Left      | Middle | Right |
| :--- | :---: | ---: |
| Text      | Text   | Text  |
```
| Left      | Middle | Right |
| :--- | :---: | ---: |
| Text      | Text   | Text  |

# Custom markdown functions
Non-expandable  
Markdown function

Custom markdown functions are called with
:md:(arg1,arg2,arg3,...) 

## Groupings
Non-expandable  
Markdown function  

Groupings are defined with :md_grouping:(id,start/end)
```markdown
Hi, I am not inside the grouping
:md_grouping:("Box","start")
Hello there, from the grouping
:md_grouping:("Box","end")
```

## Custom styling
Non-expandable  
Markdown function

You can use the ":md_style:" functions to add styling to some elements
First create/load a style :
:md_style_create:(start/end,style_id)

:md_style_define:(start/end,style_id)
:md_style_load:(file,style_id)
```
Creating a style
:md_style_create:(start,my_custom_style_1)
property1:value1;
property2:value2,
:md_style_create:(end,my_custom_style_1)

Loading a style
:md_style_load:(file,style_id)
property1:value1;
property2:value2,

Defining a style
:md_style_define:(start,custom_styles)
property1:value1;
property2:value2,
:md_style_define:(end,custom_styles)
```

You can then reference styles by id/ add them afterward

Then add styles :
:md_style_add:(id/class,style_id)
```markdown

# Heading one
:md_tag:(tag_heading)

:md_style_create:(start,style_heading)
color:red;
:md_style_create:(end,style_heading)

:md_style_add:(tag_heading,style_heading)

```


## Tagging
Non-expandable  
Markdown function  

You can tag recently created elements adding a " class="" "
inside of their html

:md_tag:(element_id)
```
Tagging an element
# Heading one
:md_tag:(heading)

you can now reference it in other functions



```








