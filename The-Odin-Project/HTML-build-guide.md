# HTML Build Guide

## Step 1 - Setup

```
<!DOCTYPE html> 
    //^ Doctype declaration

<html lang="en"> 
    //^ HTML Element `<html></html>`: Every other element in the doc will be descendant of it. Should wrap around the entire file apart from <!DOC>.
    //^anguage Attribute `lang ="en"`:  Primarily used for improving accessibility of the webpage. e.g. screen readers, adapt according to language and invoke correct prounciation.

<head>
    //^ Head Element `<head></head>`: Used to put important meta-information about the webpages and stuff required for rendering correctly in the browser. SHOULD NOT use any element that displays content on the webpage.

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
    //^ Meta Elements `<meta>`: provides metadata about the HTML doc. About data that is not displayed, for browsers and search engine
    //^ Charset Attribute `charset="UTF-8"`: Specifies the character encoding for the HTML document. Character encoding is a system that pairs each character in a script with a particular byte or sequence of bytes. To ensure the text is currectly displayed by browsers on different devices or software.

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap" rel="stylesheet">
    //^ Setup font style obtained from google font/embed code copy into head. Not done yet, in CSS > 
    body {
    font-family: 'inter', sans-serif;
}
    //^san-serif value included incase google is down.

<script src="https://kit.fontawesome.com/84cc6cb317.js" crossorigin="anonymous"></script>
    //^ Applying icon link.
    
<title>Document</title>
    //^ Title Attribute `<title></title>`Give webpage a humna-readable title, which show up on the browser tab. Without this it will use the file name which is "index.html" in most case. 
    <link rel="stylesheet" href="styles.css">
    //^ Adding CSS to HTML
</head>
<body>
    //^ Body Element `<body></body>`: Where the rest of the content goes.
    
    <script src="path/to/jsfile.js"><script>
    //^ Mostly put at the end of the <body> to ensure all content is loaded before the script runs.
    //^ alternatively you can put in the head with `defer`attribute at the end. e,g. script src="path/to/jsfile.js" defer><script>
</body>
</html>
```


## Step 2 - Body

```
<body>
    <div>
        <h1>Largest Heading</h1>
        <h6>Smallest Heading</h6>
            <p>I am paragraph</p>
            <b>Bold text</b>
            <a></a>
                //^Anchor Element: Create a link to another page or website
    </div>

<!-- -->
    <div>
        <ol>
             <li>Item 1</li>
             <li>Item 2</li>
            <li>Item 3</li>
        </ol>
    </div>

</body>
```
## Attribute
### `rel=""`
- Define the relationship between the current document and the linked document or resources. it is mostly used within `<a>`, `<link>`, `<area>` elements. 
```
<a href="https://example.com" rel="nofollow">Example</a>
//^ nofollow: Instructs search engines not to follow the link, which can be used to prevent passing SEO value to the linked page.

<a href="https://example.com" rel="noopener noreferrer" target="_blank">Example</a>
//^ noopener: Prevents the new page from being able to access the window.opener property, protecting against certain security vulnerabilities.
//^ noreferrer: Prevents the browser from sending the HTTP referrer header when navigating to the link. This also implies noopener.

<link rel="stylesheet" href="styles.css">
<area shape="rect" coords="34,44,270,350" href="https://example.com" alt="Example" rel="nofollow">
```

