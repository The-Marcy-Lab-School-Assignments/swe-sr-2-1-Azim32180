# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:

- Examples of semantic and non-semantic tags
- The differences between semantic and non-semantic tags
- The benefits of using semantic tags (when possible)

### Response 1

1. Some semantic tags include header, footer, nav, article etc. Non-semantic tags are div, span, i, br etc.
2. The main difference between the two is that semantic tags provide contextual meaning about the web-page whereas non-semantic tags are more about styling or structure without implying content type.
3. Using semantic tags:
   - provide clear context to assistive technologies that make web-pages accessible for users with disabilities.
   - improve search engine optimization that enhances the discoverability of the web-pages
   - improve readability of your code allowing effective collaboration with other developers
   - provide overall better user experience because of the clearly defined content and structure of the web-pages.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

Here are a few examples for how to make your website more accessible:

1.  Using proper semantic tags like header, nav, article etc. helps for assistive technologies to better navigate and understand the structure of your website.
2.  Providing alternative text for images is essential for people with visual impairments. Alt text describes the meaning and purpose of images, allowing screen readers to convey this information to users effectively.
3.  Some people with visual impairments rely on zoom-friendly designs. Incorporating flexible layouts that allow web pages to resize smoothly ensures responsiveness and improves accessibility.
4.  Providing sufficient color contrast helps color-blind users distinguish text from the background, improving readability.
5.  For users with hearing impairments, providing closed captions or subtitles for video and audio content is essential for accessibility.
6.  Some users cannot use a mouse, so it’s important that web pages are easily navigable by keyboard, enabling interaction with all elements on the site.

Accessibility is essential for developers to provide an equitable experience for users with visual, auditory, and motor impairments. Around 15% of the world’s population has some form of disability, making accessible design a crucial aspect of inclusive web development. Additionally, many countries have legal requirements mandating that websites be accessible. Ensuring a clear visual hierarchy, keyboard-friendly navigation, and well-structured content not only enhances usability for people with disabilities but also improves the overall user experience for everyone.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;">hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

Inline style can be handy when we need to make a quick update to the individual element in **HTML** without having to create or modify external stylesheet. This can be especially useful when doing prototyping or making temporary changes during development process.

Writing styles in a separate CSS stylesheet is crucial for maintaining clean and manageable code. It makes updating the entire website easier, ensuring consistency, readability,
and better organization of styles. This approach also improves scalability, as it's easier to maintain and extend the design system as your website grows.
Additionally, separating HTML and CSS improves collaboration among developers, allowing front-end developers to focus on structure and design independently. This separation also encourages reusability of styles and reduces redundancy in your code.

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

- An explanation of the concept of "classes" and "ids" with an analogy.
- An example of the usage using an HTML code block and a CSS code block.
- An explanation of the syntax using the terms: **attribute**, **selector**

### Response 4

Imagine you're hosting a party and you have guests arriving. You want to organize the guests in two ways:

- **Class:** Think of a class as a group of people who share a common interest or role. For example, you want to organize your guests based on their relationship to each other. You could have one table for your college friends, another for your coworkers, and a separate table for your soccer league buddies. Just like how you group people by shared characteristics, in HTML, a **class** allows you to group elements based on a common trait or purpose. You can have many **different classes**, each grouping elements that share a particular role or style, just as you have multiple groups of friends from different parts of your life.
- **ID:** Now imagine that you have a VIP guest (CEO of the company you work at). There's only one CEO at the party which allows the guest special, one-time access pass to a private lounge or VIP area. Similarly in HTML, **ID** element should be assigned to one specific element only that distinguishes from the rest of the elements.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Class Example</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <!-- Grouping elements by class -->
    <h1 class="college-friends">Greetings, college friends!</h1>
    <p class="college-friends">
      Welcome to my party! Please take a seat on Table #1
    </p>

    <h1 class="coworkers">Hello, Coworkers!</h1>
    <p class="coworkers">Welcome to my party! Please take a seat on Table #2</p>

    <h1 class="soccer-friends">Hey, Soccer Team!</h1>
    <p class="soccer-friends">
      So great ya'll could come! Please take a seat on Table #3
    </p>

    <!-- Using ID for a unique element-->
    <div id="ceo">
      Good evening Mr. Vonderloo, please follow me to your private lounge
    </div>
  </body>
</html>
```

```css
/* Styling all elements with the class "college-friends" */
.college-friends {
  color: green;
  font-weight: bold;
}

/* Styling the unique element with the ID "ceo" */
#ceo {
  color: gold;
  font-size: 24px;
  text-align: center;
}
```

- In HTML, you can assign a class to an element using the class attribute. In CSS, you can select the class by using a dot selector followed by a class name.

```html
HTML
<p class="college-friends"></p>
```

```css
CSS .college-friends {
  ...;
}
```

- In HTML, you assign an ID to an element using the id attribute, and in CSS you can select the **ID** by using a hash (#) selector followed by the ID name:

```html
HTML
<div id="ceo"></div>
```

```css
CSS #ceo {
  ...;
}
```

To conclude, a **class** can be applied to multiple elements on the page. Like having diverse circle of friends.
An **ID** should be used for a unique element on the page, like the CEO who is one-of-a-kind hot shot dude.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

No, it is not best practice to build an entire website using only JavaScript and the DOM API. HTML and CSS should be used for defining the **structure** and **styling** of your website, as they are best suited for static content, layout, and visual design. These form the foundation of your site, ensuring it is accessible and properly structured.

On the other hand, **JavaScript** and the **DOM API** should be used to add **interactivity**, dynamically modify content, and handle **real-time user interactions**. For example, dynamic behaviors such as a "like" button that toggles between "like" and "dislike" states, or form validation that checks input when a button is clicked, can only be achieved with JavaScript.

Additionally, JavaScript is essential for tasks like loading dynamic content from external servers (e.g., displaying product details from an API), making real-time updates (e.g., notifications, live scores), and handling user-driven interactions on the website (e.g., interactive forms, buttons, likes, comments and animations).

In summary, HTML/CSS is used for static content and layout, while JavaScript and the DOM API handle dynamic behavior and user interactions. Combining both effectively ensures a well-structured, responsive, and interactive website.
