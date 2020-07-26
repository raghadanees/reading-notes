

## Text

#### Headings and paragraphs

*HTML has six "levels" of headings <h1> <h2> <h3> ...
*Paragraph: To create a paragraph, surround the words that make up the paragraph with an opening <p> tag and closing </p> tag.


#### Bold, italic, emphasis
By enclosing words in the tags  <i> and </i>  we can make characters appear italic.
 By enclosing words in the tags ` <b> and </b> ` we can make characters appear bold.
 Line Breaks & Horizontal Rules: if you wanted to add a line break inside the middle of a paragraph you can use the `line break tag <br />`.

#### Structural and semantic markup
Quotations: The `<q>` element is used for shorter quotes that sit within a paragraph.
The `<s>` element indicates something that is no longer accurate or relevant (but that should not be deleted).

HTML   |  Result
---------|--------
`<p>Laptop computer:</p>`   | <p>Laptop computer:</p>
 `<p><s>Was $995</s></p>`   | <p><s>Was $995</s></p>
 `<p>Now only $375</p>`     | <p>Now only $375</p>

 ### CSS works by associating rules with HTML elements. 
 These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.
- Selectors indicate which element the rule applies to.
The same rule can apply to more than one element if you separate the element names with commas.
- Declarations indicate how the elements referred to in the selector should be styled.
Declarations are split into two parts (a property and a value), and are separated by a colon.
- The `<link>` element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the `<head>` element.
ex: `<link href="css/styles.css" type="text/css" rel="stylesheet" />`
- #### Using Internal CSS
You can also include CSS rules within an HTML page by placing them inside a <style> element, which usually sits inside the <head> element of the page.
`<style type="text/css"> `
`body {`
`font-family: arial;`
`background-color: rgb(185,179,175);}`
`h1 {`
`color: rgb(255,255,255);}`
`</style>`

## JS
A script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement.
Statements should end with a semicolon.
JavaScript is case sensitive so hourNow means something different to HourNow or HOURNOW.
To write a comment that stretches over more than one line, you use a multi-line comment, starting with the /* characters and ending with the * / characters.
A script will have to temporarily store the bits of information it needs to do its job. It can store this data in *variables*.
