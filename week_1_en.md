# WEEK 1: Introduction & Basic HTML

## Website development overview (Binh)

### What is a Frontend developer?

Front-end web development, also known as client-side development is the practice of producing HTML, CSS and JavaScript for a website or Web Application so that a user can see and interact with them directly.

### What is UI/UX?

UX design refers to the term “user experience design”, while UI stands for “user interface design”. Both elements are crucial to a product and work closely together. But despite their professional relationship, the roles themselves are quite different, referring to very different aspects of the product development process and the design discipline.

- What is user experience (UX) design?

  User experience design is a human-first way of designing products. Don Norman, a cognitive scientist and co-founder of the Nielsen Norman Group Design Consultancy, is credited with coining the term “user experience” in the late 1990s. Here’s how he describes it:

  > “User experience encompasses all aspects of the end-user’s interaction with the company, its services, and its products.” – Don Norman, Cognitive Scientist & User Experience Architect

- What is user interface (UI) design?

  While user experience is a conglomeration of tasks focused on the optimization of a product for effective and enjoyable use, user interface design is its complement; the look and feel, the presentation and interactivity of a product.

#### How websites work in a nutshell

When you type a web address into your browser (for our analogy that's like walking to the shop):

1. The browser goes to the DNS server, and finds the real address of the server that the website lives on (you find the address of the shop).

2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client (you go to the shop and order your goods). This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.

3. If the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called data packets (the shop gives you your goods, and you bring them back to your house).

4. The browser assembles the small chunks into a complete web page and displays it to you (the goods arrive at your door — new shiny stuff, awesome!).

#### Communicate between backend and frontend

Frontend and backend communicate with each other - via Http requests. The frontend will, for example, send entered data to the backend. The backend might then again validate that data (since frontend code can be tricked) and finally store it in some database.

The magic is within the HTTP request/response payloads. The backend usually responds with certain contents of the HTTP body:

- HTML-formatted responses
- other static files (CSS, JS, images, …)
- JSON-formatted data
- No body at all. Just a status code and header fields.

The frontend sends:

- Simple HTTP requests without a body
- Form data
- JSON-formatted data

## Terminal (Quan)

## Version control (Git) (Quan)

### Gitflow

The overall flow of Gitflow is:

1. A `develop` branch is created from `main`
2. A `release` branch is created from `develop`
3. `Feature` branches are created from `develop`
4. When a feature is complete it is merged into the `develop` branch
5. When the `release` branch is done it is merged into `develop` and `main`
6. If an issue in `main` is detected a `hotfix` branch is created from `main`
7. Once the `hotfix` is complete it is merged to both `develop` and `main`

## HTML5 (Tuan)

### How to structure HTML

Each and every HTML 5 document employs a unique combination of elements and content to define a page. The structure of all the property documented pages is the same and contains:

1. A declaration at the top, which indicates that it is an HTML 5 document
2. A document header
3. A document body

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Basic Page Structure</title>
  </head>
  <body>
    <!-- HTML Element -->
  </body>
</html>
```

`<!DOCTYPE>` informs the browsers that it is actually an HTML 5 document. Although there are other types of DOC Types, this is the most commonly used declaration.

The DOCType Declaration is followed by `<html></html>` opening and closing tags. These tags contain everything inside the document, including the Head and Body

`<head> </head>` opening and closing tags, follow the opening Html tag. These tags contain information about the body, title of the page, definitions, labels, etc. You can only use certain markup elements in the HTML 5 head. Some of these elements include style, title, base, link, script, and meta. In HTML 5, these elements are collectively known as HTML Head Elements.

After the closing head tag is the `<body> </body>` opening and closing body tags. They contain all the content which appears on the browser, as well as the related HTML 5 codes

### Import script, style to the website

- Import script

  The `<script> </script>` tag is what we use to includes our JavaScript.

  ```html
  <script type="text/javascript">
    alert('This alert box was called with the onload event');
  </script>
  ```

  Using the script tag to include an external JavaScript file.

  To include an external JavaScript file, we can use the script tag with the attribute src. You've already used the src attribute when using images. The value for the src attribute should be the path to your JavaScript file.

  ```html
  <script type="text/javascript" src="path-to-javascript-file.js"></script>
  ```

  This script tag should be included between the `<head>` tags in your HTML document.

- Import style

    CSS can either be attached as a separate document or embedded in the HTML document itself. There are three methods of including CSS in an HTML document:

  - Inline styles — Using the style attribute in the HTML start tag.

  ```html
  <h1 style="color:red; font-size:30px;">This is a heading</h1>
  <p style="color:green; font-size:22px;">This is a paragraph.</p>
  <div div style="color:blue; font-size:14px;">This is some text content.</div>
  ```

  - Embedded styles — Using the `<style>` element in the head section of a document

  ```html
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>My HTML Document</title>
      <style>
        body {
          background-color: YellowGreen;
        }
        p {
          color: #fff;
        }
      </style>
    </head>
    <body>
      <h1>This is a heading</h1>
      <p>This is a paragraph of text.</p>
    </body>
  </html>
  ```

  - External style sheets — Using the `<link>` element, pointing to an external CSS file.

    An external style sheet is ideal when the style is applied to many pages of the website.
    An external style sheet holds all the style rules in a separate document that you can link from any HTML file on your site. External style sheets are the most flexible because with an external style sheet, you can change the look of an entire website by changing just one file.
    You can attach external style sheets in two ways — linking and importing.
    - Linking External Style Sheets

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>My HTML Document</title>
        <link rel="stylesheet" href="css/style.css">
    </head>
    <body>
        <h1>This is a heading</h1>
        <p>This is a paragraph of text.</p>
    </body>
    </html>
    ```

    - Importing External Style Sheets

    ```css
    @import url("css/layout.css");
    @import url("css/color.css");
    body {
        color: blue;
        font-size: 14px;
    }
    ```
