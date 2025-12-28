# UFV • Practical Work II — Personal Website 
Author: Borja Rincón Lozada  
Course: Fundamentals of Computer Engineering (FCE)  
Technologies: HTML, CSS,  JavaScript  
Project type: website

----------------------------DESCRIPTION-----------------------------------------
Practical Work II — Personal Website
1) What this project is

This repository contains a static personal website developed as part of Practical Work II for the subject Fundamentals of Computer Engineering (FCE).

The website is static, which means:

It is composed of HTML files

Styled using CSS

Uses basic JavaScript for interaction

It has no backend, no database, and no server-side logic

All logic runs directly in the browser.

The main objective is to apply the theoretical concepts learned in the subject (HTML structure, CSS layout, basic JavaScript, Git usage and project organization) in a complete and coherent web project.


2) Project structure and organization

/
├── index.html
├── public/
│   ├── about.html
│   ├── degree.html
│   ├── fce.html
│   ├── topic.html
│   ├── net.html
│   └── contact.html
├── images/
└── FCE/

Why this structure?

index.html is the main entry point

The public/ folder contains all internal pages, keeping the root clean

images/ stores shared visual assets

FCE/ groups PDFs and academic material related to the subject

This structure improves clarity and avoids mixing content types.
And most important, is the structure you told us to do Moises :d

3) Relative paths and navigation

Because pages are in different folders, relative paths are required.

Example from a page inside public/:
<img src="../images/ufv_logo.png" alt="UFV logo">
../ moves one directory up before accessing images/.

This was one of the most common issues during development, as incorrect paths caused broken images and links.4) Global design system

To ensure visual consistency, all pages define shared CSS variables:

:root {
  --bg: #0f1424;
  --panel: #151b2f;
  --text: #f2f4ff;
  --muted: #b8bdd6;
  --border: rgba(255,255,255,.12);
  --accent: #2f6bff;
  --radius: 14px;
}
Why use CSS variables?

Same colors and spacing across all pages

Easy global changes

Less repeated code

Base rules are also defined:
* { box-sizing: border-box; }
body { margin: 0; }
a { color: inherit; }

This avoids browser defaults interfering with the design.

5) Reusable components
5.1 Topbar (navigation)

The topbar appears on every page and uses:
.topbar {
  position: sticky;
  top: 0;
  z-index: 10;
}
Purpose:

Keep navigation visible while scrolling

Improve usability

Highlight the current page with an active state

Flexbox is used to align brand and navigation links.

5.2 Cards

Cards are used as the main content container:
.card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 16px;
}

They visually separate sections and keep the design consistent.

5.3 Buttons and links

Most actions are <a> elements styled as buttons, because navigation is the primary interaction.

Primary buttons use the accent color to indicate importance.

5.4 Footer

The footer includes:

Social links (GitHub and LinkedIn)

Copyright information

It follows common web conventions and completes the page structure.

6) Layout techniques

Two main layout systems are used:

CSS Grid

Used for page-level layouts and galleries:
.hero {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
}

Flexbox

Used for alignment inside components (menus, rows, icon groups).

This combination allows clean, responsive layouts.

7) Responsiveness

Media queries adapt the layout for smaller screens:
@media (max-width: 900px) {
  .hero { grid-template-columns: 1fr; }
}

This ensures:

Mobile compatibility

Better readability

Compliance with the assignment requirements

8) Page overview

Home (index.html): introduction, goals and navigation

About: personal profile, motivation, CV and social links

Degree: explanation of the degree using sections and accordions

FCE: subject hub with tabs for description, units and practical work

Topic: academic topic explained using <details> blocks

Net: gallery of classmates’ websites

Contact: front-end contact form and alternative contact methods

JavaScript is used only where necessary to manage visibility and interaction.

9) Git workflow and commands

Git was used to track progress and manage changes.

Typical workflow:
git status
git add whatever the  file was
git commmit -m 
git push

In this section a problem was presented, that was the number of commits, I exceded it, because I was doubting abput when to do the commits so I just did it while doing it.
10) Accessibility and usability

Images include alt text

Hover states provide visual feedback

Clear hierarchy of titles and text

Consistent navigation across pages

Final note: Why this documentation is  like this

This documentation is intentionally a little bit more detailed. Beyond fulfilling the academic requirements of the assignment, I used the process of explaining every component as a learning tool for myself. Writing down what each element does, why it is used, and how it interacts with the rest of the website helped me to understand the concepts instead of simply applying them mechanically. By forcing myself to justify design choices, layout decisions, and technical implementations, I reinforced my understanding of HTML, CSS, JavaScript, and Git. So in order to not get lost, I was writing down things I didnt understand at first, so when time past, I didnt forget what was it, or the purpose in case that it was generating an error.



-------------PROBLEMS-------------------------------------------------------------------------------------
I faced Couple of problems during the development of the website:

1. The Pushes
Because I still get confused about how and when I have to do the pushes. So I ended making more than 6 pushes, to make sure 
it is all documented

2. Image size not updating
At some point, changing the image size in CSS had no visible effect. This happened because the CSS selector was not targeting the correct element or was being overridden by a more specific rule defined later in the stylesheet.

3. Non-functional links (href="#")
Some resource links initially used href="#", which does not lead to any real content. This caused confusing user interaction and required replacing them with valid external URLs.

4. Resource images alignment and spacing
Images inside the resources section appeared too close together or stacked incorrectly. This was fixed by applying a proper flex layout with spacing and wrapping for responsive behavior.

5. Relative path issues (../)
Because the project uses multiple folders (index.html in root and pages inside /public), some images and links initially broke due to incorrect relative paths.

6. Invalid HTML structure (duplicate or misclosed tags)
Some pages contained duplicated footers or extra closing tags, which resulted in invalid HTML and unpredictable layout behavior in browsers.

7. Broken or inconsistent navigation links
There were inconsistencies in page names, which could cause broken navigation links in the topbar. And I lost a lot of time because of this errors.

8. Repeated inline CSS across pages
Each page contained its own <style> block. While functional, this made maintenance harder and increased the risk of inconsistencies between pages. 

9. Minor language and spelling errors
Several small English mistakes appeared in headings and text content, which could reduce clarity and professionalism if not corrected.

10. Contact form without backend functionality
The contact form does not actually send messages. This is not a technical bug, but it must be clearly stated to avoid user confusion.

11. Accessibility and semantic limitations
Some elements (such as disabled links or clickable cards) lacked full semantic meaning or accessibility optimization, which could affect usability and evaluation.

12. Because I was doing late the website, i couldnt reach for any other websites, so in network I put other peers websites but from last year.


--------------CONCLUSION---------------------------
This project represents a complete practical application of the concepts learned in Fundamentals of Computer Engineering, combining HTML and CSS to build a structured, navigable, and visually consistent website. Throughout the development process, several technical and structural issues were encountered and resolved, reinforcing the importance of debugging, file organization, and CSS hierarchy. The final result demonstrates an improved understanding of layout design, responsive behavior, and component reuse. Despite its limitations (such as the absence of backend functionality), the website fulfills the academic objectives of the assignment and serves as a solid foundation for future web development projects.