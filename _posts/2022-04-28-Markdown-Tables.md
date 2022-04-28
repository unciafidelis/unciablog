---
layout: post
title:  "Markdown headers and tables"
date:   2022-04-28 17:02:14 -0500
categories: Markdown
---

# MarkDown Sintaxis básica - Tablas y encabezados 

### The hidden art of writing project documentation on github

To teach myself how to use Markdown i was forcing myself to replicate every aspect of the official page [Markdown](https://www.markdownguide.org/basic-syntax/) but showing the code (wink*), of course this will not be an easy task, but I will concentrate on each topic to make it more digestible so let's start with the first table, the headings table.

To make this table, I first need to know how to make a table, right? so i did this google search:

`how to make a table in Markdown`

and it took me directly to the answer, the page [Hackmd](https://hackmd.io/s/how-to-create-table) with the example:

html = markdown(s, extensions=['tables'])

|Name |Quantity
|:----:|:----:
|Apple|3       
|Egg  |12      

which in code would be:

```markdown
|Name|Quantity
|:----:|:----:
|Apple|3       
|Egg  |12      
```
By the way, to see the code, you just have to use the following:


\```markdown(here you can also put javascript for example and thus it will format it as javascript)
   here is the markdown code
\```

Triple backticks(Yes, that's what they're called...) mark the beginning and the end of the code, while markdown in this case, represents a language. The use of the \ was to bypass the markdown formatting in order to be able to place the backticks and that they all look nice there, if I didn't they would only see the "markdown code goes here" in the section.

Well, now that we know how to make a table, we just have to empty the data of how to make a header and its result:

|Markdown|HTML| Rendered Output   
|:----:|:----:|:----:
|# Heading     |Tag H1|<h1>Heading</h1>  	
|## Heading    |Tag H2|<h2>Heading</h2>	
|### Heading   |Tag H3|<h3>Heading</h3>	
|#### Heading  |Tag H4|<h4>Heading</h4>	
|##### Heading |Tag H5|<h5>Heading</h5>	
|###### Heading|Tag H6|<h6>Heading</h6>	


The table is slightly different from the original but for me it is better understood hehe.
Now the code:

```markdown
|Markdown|HTML| Rendered Output   
|:----:|:----:|:----:
|# Heading     |Tag H1|<h1>Heading</h1>  	
|## Heading    |Tag H2|<h2>Heading</h2>	
|### Heading   |Tag H3|<h3>Heading</h3>	
|#### Heading  |Tag H4|<h4>Heading</h4>	
|##### Heading |Tag H5|<h5>Heading</h5>	
|###### Heading|Tag H6|<h6>Heading</h6>	
```
As we can see the numeral symbol (this lil fella #) adds a level to the font size making it smaller with each added numeral, that as in HTML syntax, as the number of H increases (<H(number of h)>) its size decreases.

Note that there is a space between the numeral and the header name, if you omit it, this will happen:

#This has no space but a numeral

contrary to:

# This DOES have a space and a numeral

there is another way to make headers but no sane person would use it... so for all of us to keep sanity and practicality let's stick with this simple method.

Now you know how to make tables and headers in Markdown! WHAT!?
