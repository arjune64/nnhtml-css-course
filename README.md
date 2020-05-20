# Net Ninja HTML, CSS Course

## 01_Introduction

1.HTML is the markup language to structure content
2.CSS is the language for styling web pages.
3.HTML tags are used for structuring the content on a web page.

## 02_HTML Basics
### HTML Tags - The HTML document is composed of a tree of HTML elements or tags. All the elements are represented using a opening tag and a closing tag. (< ></ >)

Common html elements

1. P - paragraph tag
   Used for writing paragraph text

2. h - heading tag
  Used for writing headings on a page. Headings tags are represented from h1 to h6 in the decreasing order of the text size.
3. small - small tag
  Used to make the text smaller
4. Strong - strong tag
  Used to make the text bold
5. ul - stands for unorderd list
  used for making bulletted lists

      ```
    syntax: 
      
      <ul> 
        <li></li>
      </ul>
      ```
6. a - anchor tag
  used for adding hyperlinks
7. blockquote - used for adding block quotes
      The items should be listed will be between and opening and closing ul tags
6. div - division tag
  div tags makes division between elements. there will be no visual effect 
7. span - span tag
  it is an inline element 
8. br - line break
  for amking line breaks between elements
9. hr - horizondal rule
  for making a horizondal line
10. img - image tag
  for inserting a image to the web page

11. Attribute - something inside an element which have sme property
  
  eg: href - for adding hyperlinks

## 03_HTML Forms

  ```
  syntax
  `<form> 
  <label for="ID">name</label>
  <input type = "text", id="name">
  </form>`
  ```
## 04_CSS Basics
## 05_CSS classes and selectors.


1. class selector - to specifically select a tag.  
   
   ```
  eg:<p class="name">Hello world</P>
  ```
```
   	syntax: .name { }
     ```

if we select p.name { } - This will only select the p tag with the      class name = name
we can also use multiple class names for a tag

  ```
  eg: <p class="name hello">Hello world</P>
  ````
```
   	syntax: p.name.hello { } 

     ```
	
2. ID selector
 
 ```
  eg: <p id ="name"> hello world  </p>

  syntax = #name {}
```
3. descendant selector - selects the child element of a parent element

```
  	eg: div p {

  	will select only p tags of a div 
  }

	````

4. attribute selectors

	eg: a[href]

  To select a href attribute with a specific href value

  eg: a[href="https://thenetninja.co.uk"] will select all href with the value 'https://thenetninja.co.uk
  
    or 
  
  a[href*="thenetninja"] means any href starts with the net ninja

  a[href$="thenetninja"]` means any href ends with the net ninja.

### The cascade

HTML elements can inherit css properties that are applied to their parents

```
  eg: <div>
  	<p></P>
      </div> 

	```
  If we apply a style to the div element
  Div {
  color: red;
  }
  
  ```


Font properties can only be inherited.

#### Specificity and precedence.

```
* Div {
	Color: orange;
	}

* P {
Color: cinnamon;
}

* Div.p {
Color : tomato;
}

```

the 3rd one is more specific than others so this will have first priority than others, followed by 2 and 1.

Doubt

1. Why to use multiple class names for a class
2. diff between descendant selector and multiple class selector

## 06_HTML Schematic Tags

#### Used for a better structuring of the HTML page or making the code more meaningful.

```
  <main> - for the main content of a webpage. This is unique to a webpage.
  eg - navigation tab

  <section> - Defines a certain section of a webpage.
  eg - contact, blog list

  <article> - defines a bit of content which makes up an article
   eg - a blog post
  <aside> - defines some content related to something else
  Eg - similar blogs
  <header> - for the header of a website - contains the nav, title etc..
 
  <footer> - for the footer of a website
  <nav> - for navigation links
    eg: ul
```

## 07_Chrome Development tools

1. elements tab - list all the html tags and its properties
2. If any rule is cross ruled it means this is over written by a new rule
3. Sources tab - shows all the source files of the project  

## 08_CSS Layout and Position

  CSS Positions

    * Static
    * Relative
    * Fixed
    * Absolute
    * Sticky

1. static - This is the default value

2. Relative - Means we can shift the element relative to the original position in the page

	```
  eg: {
  Position: relative;    
  Left : 20px;
  bottom:20px
  } 
  	
	```

  This will shift the elements 20px to left and 20px from bottom.

3. Fixed - will position the element fixed even if we scroll the page down.

	```
  eg: {
  Position: fixed;    
  Left : 0px;
  Bottom: 0px
  } 
  
	```
  This will put the elements in a fixed position.


4. Absolute - will position the element relative to its closest parent.

```
	eg: {
  Position: absolute;    
  Left : 20px;
  Bottom: 20px;
  }
  
  ```

5. Sticky - it is a mixture of static and fixed.

  It takes a value from top or bottom and when that value is achieved this will stick on that.
  ```
  Eg: nav {
  Position: sticky;
  Top:148px;
  }
  The nav bar will stick on the page when the value 148px is achieved from the top.
  ```
## 09_Pseudo classes 
### style elements when they are in a particular state
#### hover, focus,first child of a parent


1. hover pseudo class - hover means when draw the crusor over a link or image

```
nav li a:hover {
text-decoration:underline; - to get a underline effect when we hover over the a tags 
}

```
	```
images li:hover {
position:relative;  - images will shift 4px upwards when we hover over the images
top:-4;
}

```

2. focus pseudo class - focus means when we click a form field or a link

````

form input:focus {
border:4px dashed #4b4b4b;
outline:none;
}

```

3. valid pseudo class - valid is used to identify the user input is valid or not

eg: if we enter a email address into a form field, if it is not in the correct format 

```

form input:focus {
border:4px solid #71d300;
}

```

4. first child pseudoclass - we can tag the first child of a parent element with this pseudoclass

```
nav li:first-child {
  border: 4px solid #f63232; - this will draw a border for the first child of the nav bar.
}

```

5. Pseudo elements

##### Used to insert content dynamically before or after a element

```

eg:

article p::first-line {
  font-weight: bold;	- This will make the first line of the p tag of article section to bold and increase the size of the font to 1.2em.
  font: 1.2em;
}

section.join p::first-letter {
  font-size: 1.5em;		- This will increase the text size of the first letter to 1.5em.
}

```

6. p::selection {
  background-color: #f63232;	- this will  make the background color to #f63232 and text color to white when we select a paragraph content 
  color: white;
}


7. p::after {
  content: '...';   - this will add '...' after every p contents using the property content.
}


8. p::before {
  content: '...';   - this will add '...' after every p contents using the property content.
}

```


## 10_Media query - tell the browser hoe to style an element at particular viewport dimensions 13:16

1. viewport meta tag - tells the browser what width the viewport should be

2. meta tag - <meta name="viewport" content="width=device-width, initial-scale=1.0">







