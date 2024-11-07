# ANCAR-MARKDOWN -- RULES 📑

### 📜 Index
1. [Headings](#headings)
2. [Text Quick Styling](#text-quick-styling)
3. [Tables](#tables)
4. [Custom Markdown Functions](#custom-markdown-functions)
5. [Groupings](#groupings)
6. [Custom Styling](#custom-styling)
7. [Tagging](#tagging)

---

## Headings {#headings}
**Expandable**  
Supports six levels of headings from 1 to 6. Follow the syntax below:

| Syntax | Heading Size |
|--------|--------------|
| `#`    | 1           |
| `##`   | 2           |
| `###...` | ...      |

## Text Quick Styling ✍️
**Expandable**  
Multiple text styling options with the following default syntax:

| Syntax           | Result          |
|------------------|-----------------|
| `~~text~~`       | ~~text~~        |
| `*text*`         | *text*          |
| `**text**`       | **text**        |
| ...              | ...             |

## Tables 📊
**Non-expandable**

```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

To set alignment with colons ":" use the syntax below:

```
| Left      | Middle | Right |
| :---      | :---:  | ---:  |
| Text      | Text   | Text  |
```

| Left      | Middle | Right |
| :---      | :---:  | ---:  |
| Text      | Text   | Text  |

## Custom Markdown Functions ⚙️
**Non-expandable**  

Custom markdown functions are called with `:md:(arg1,arg2,arg3,...)`

---

## Groupings 📦
**Non-expandable**  
Markdown function for grouping text or elements. Use `:md_grouping:(id,start/end)` for grouping:

```
Hi, I am not inside the grouping  
:md_grouping:("Box","start")  
Hello there, from the grouping  
:md_grouping:("Box","end")  
```

---

## Custom Styling 🎨
**Non-expandable**  
Use `:md_style:` functions to add styling to elements. To define, create, or load a style, use the following format:

```
Creating a style  
:md_style_create:(start,my_custom_style_1)  
property1:value1;  
property2:value2;  
:md_style_create:(end,my_custom_style_1)  

Loading a style  
:md_style_load:(file,style_id)  
property1:value1;  
property2:value2;  

Defining a style  
:md_style_define:(start,custom_styles)  
property1:value1;  
property2:value2;  
:md_style_define:(end,custom_styles)  
```

Once defined, reference styles by id or add them later:

```
# Heading one  
:md_tag:(tag_heading)  

:md_style_create:(start,style_heading)  
color:red;  
:md_style_create:(end,style_heading)  

:md_style_add:(tag_heading,style_heading)  
```

---

## Tagging 📌
**Non-expandable**  
Use the `:md_tag:` function to add a "class" attribute to an element:

```
Tagging an element  
# Heading one  
:md_tag:(heading)  

You can now reference it in other functions  
```

--- 

This readme covers essential guidelines and advanced customization for using the ANCAR-MARKDOWN syntax.
