ISAIAH'S PORTFOLIO (INFR3120 ASSIGNMENT 1)
==========================================

This is my personal portfolio site for INFR3120. It's built with plain HTML5 and CSS3, and it's hosted on GitHub Pages.

Live site: [paste your GitHub Pages link here]
Repository: [paste your GitHub repo link here]


PAGES
-----
There are four separate HTML files, no single page app.

index.html    - Home page with my intro, my photo and a timeline of my experience (past, present, future)
about.html    - Poster style About Me layout with clickable notes that open popups, my intro video, and the same timeline
projects.html - Five projects, each with a heading and a short explanation
contact.html  - Contact form with validation

Every page has the same header with the nav bar and the same footer with my email and copyright.


FOLDER STRUCTURE
----------------
portfolio/
  index.html
  about.html
  projects.html
  contact.html
  README.txt
  css/
    mobile.css    (phones)
    tablet.css    (tablets)
    laptop.css    (laptops and desktops)
  images/         (my photos and the video poster image)
  videos/         (my intro video)


RESPONSIVE DESIGN
-----------------
The site is fluid. I used percentage widths, a centered wrapper with a max-width, and clamp() for the big headings so they grow and shrink with the screen. I did not use Flexbox anywhere. Where I needed columns I used float and inline-block, and for the About page poster I used absolute positioning inside a box that keeps the same shape as it scales.

Each page loads only one of the three stylesheets, depending on the screen width. The media attribute on each link tag decides which one loads. Each file holds the full styles for its screen size.

mobile.css
  Width: up to 480px
  Why: Covers phones in portrait, which are roughly 320px to 430px wide. Everything stacks into one column and the nav centers.

tablet.css
  Width: 481px to 960px
  Why: Covers tablets and large phones turned sideways. There's room for two columns, but it's tight, so I reduced the padding.

laptop.css
  Width: 960px and up
  Why: A 960px layout fits comfortably on laptops and desktops, so this is where I use three columns and wider spacing.

I used these breakpoints because they're the ones from our lectures.


GRADIENTS
---------
Linear gradient (left to right):
  - the thin bar under the header on every page
  - the underline below the main headings on the Projects, Contact and timeline sections

Angled linear gradient (135deg):
  - the round logo badge in the header
  - the blob shape behind my photo on the home page
  - the selected symbol on the About page [update this if you changed it]


COLOR SCHEME
------------
I started from Future Blue on Adobe Color (https://color.adobe.com/create) using the complementary rule, which gave me the orange to go against it. [Add a screenshot of your Adobe Color wheel to the repo and mention the file name here.]

Future Blue     #003C71   Headings inside cards, logo gradient, footer
Simcoe Blue     #0068B8   Logo gradient, hover states, the Present arrow in the timeline
Tech Tangerine  #E75D2A   Card top borders, the Submit button, gradient accents, nav underline
Light Blue      #EAF2FA   Form fields, project tags, card backgrounds
Nardo Grey      #6B6D70   Page background

Text is near black (#030303) or white. I put white text straight on the grey and dark blue text inside the white and light boxes, because dark blue on the grey was too hard to read.


HOW THE TIMELINE AND POPUPS WORK
--------------------------------
The timeline and the About page popups use no JavaScript. Each one has hidden radio buttons, and each clickable label points to one radio button with the for attribute. When you click a label, the browser checks that radio button, and the CSS shows the matching section using the :checked selector and the ~ sibling selector. That's why the radio buttons come before the labels and content in the HTML.


CONTACT FORM VALIDATION
-----------------------
The validation is all HTML5 attributes, no JavaScript.
  - Name is required and needs at least 2 characters.
  - Email uses type="email" so the browser checks the format.
  - Cell No. uses a pattern that accepts 10 digits, with optional hyphens (905-555-1234).
  - Message is required and needs 10 to 500 characters.
  - The "2+2" question only accepts the answer 4.

GitHub Pages can't process forms, so the form uses a mailto: link. It opens the visitor's email app with the message filled in.


TESTING
-------
HTML validation (W3C Markup Validator): [errors / warnings per page]
CSS validation (W3C CSS Validator): [errors / warnings]
Link check (W3C Link Checker): [result]
Spelling ([tool you used]): [result]
Accessibility (WAVE): [result, and anything you fixed]


CREDITS AND SOURCES
-------------------
  - Fonts: Poppins, Caveat and Playfair Display from Google Fonts (https://fonts.google.com).
  - Icons on the About page are standard emoji, so there are no image files for them.
  - Code from lectures: [list anything you reused from class].
  - Other code I looked up: [name the site and what you used it for, for example the W3Schools page on responsive floats]. This is under 10 percent of my code.
  - [If your course says to cite AI tools, add a line here saying which tool you used and for what.]
  - The photos and the intro video are mine.
