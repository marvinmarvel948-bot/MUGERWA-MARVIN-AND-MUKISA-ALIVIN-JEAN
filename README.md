# MUGERWA-MARVIN-AND-MUKISA-ALIVIN-JEAN
COURSE PROJECT TO BE PRESENT ABOUT BRIGHT HIGH SCHOOL WEBSITE

BRIGHT HIGH SCHOOL LUWERO GULU - WEBSITE PROJECT 


---------------------------------------------------------------------
1. PAGES
---------------------------------------------------------------------
index.html         Home           Hero, welcome, explore cards, apply band,
                                  prospectus request form
about.html         About Us       Story, mission and vision, values,
                                  
academics.html     Academics      Learning stages, curriculum table
                                  (rowspan/colspan), assessment
admissions.html    Admissions     Steps, requirements, fees table, key
                                  dates, online application form, FAQ
services.html     Programmes       Supporting services for learners and
                                  families
student-life.html  Student Life   Sports, clubs, boarding, community,
                                  Drama club video
gallery.html       Gallery        Photo grid with alt text and captions
media.html         Media Centre   Captioned school introduction video
faq.html           FAQ            Expandable questions (details/summary)
contact.html       Contact Us     Contact details, enquiry form, map

All pages share one stylesheet (css/style.css) and the same top bar,
header, navigation, page banner and footer.


---------------------------------------------------------------------
2. FOLDER STRUCTURE
---------------------------------------------------------------------
bright-high-school-luwero-gulu/
|-- index.html
|-- about.html
|-- academics.html
|-- admissions.html
|-- services.html
|-- student-life.html
|-- gallery.html
|-- media.html
|-- faq.html
|-- contact.html
|-- README.txt
|-- css/
|   `-- style.css
|-- images/
|   |-- classroom assembly.jpg
|   |-- classroom-reading.jpg
|   |-- sports-day.jpg
|   |-- music-club.jpg
|   |-- boarding-dormitory.jpg
|   |-- science-club.jpg
|   |-- library.jpg
|   `-- community-service.jpg
`-- media/
    |-- school-introduction.mp4
    |-- school-introduction-en.vtt
    |-- drama-club.mp4
    `-- drama-club.webm

Relative paths (css/style.css, images/..., media/...) only work if this
structure is kept. Do not move files without updating the paths.


---------------------------------------------------------------------
3. HOW TO RUN
---------------------------------------------------------------------
1. Unzip the project folder.
2. Open index.html in any modern browser (Chrome, Edge, Firefox,
   Safari). No server or installation is needed.
3. Use the main menu to move between pages.

To publish, upload the whole folder to any static host (shared
hosting, GitHub Pages, Netlify) over HTTPS.


---------------------------------------------------------------------
4. DESIGN SYSTEM (css/style.css, about 840 lines)
---------------------------------------------------------------------
Colours (CSS custom properties on :root)
  --primary        #123b70   deep blue: top bar, banners, headers
  --primary-dark   #0b2850   dark end of gradients, button hover
  --primary-soft   #e8f0fb   text on dark blue backgrounds
  --accent         #5b8def   light end of gradients
  --accent-strong  #356fd6   kickers, menu underline
  --ink            #172235   body text
  --ink-soft       #45546a   secondary text
  --ink-muted      #6c7a90   captions
  --bg-soft        #f5f8fd   alternate section background
  --border         #dce5f0   borders
  --focus          #3978e8   keyboard focus outline

Font      Inter, then system fonts (nothing is downloaded)
Spacing   --sp-1 8px, --sp-2 14px, --sp-3 20px, --sp-4 25px,
          --sp-5 40px, --sp-6 60px
Layout    Flexbox (header, cards, footer) and CSS Grid (hero, gallery)
Breakpoints  900px (tablet), 600px (phone), 360px (very small phone)
Extras    Sticky header above 900px, menu that scrolls sideways on
          phones, optional dark theme (add data-theme="dark" to <html>)

The stylesheet has two layers: a base layer and an "advanced UI layer"
at the end of the file that overrides the tokens and adds polish.


---------------------------------------------------------------------
5. ACCESSIBILITY FEATURES
---------------------------------------------------------------------
- Skip link at the top of every page (jumps to #main)
- Semantic landmarks: header, nav, main, footer
- One h1 per page, headings in order
- aria-current="page" on the active menu link
- Visible 3px keyboard focus outline
- Alt text on images; captions track and text alternative for video
- Labelled form fields, fieldset/legend, native validation
- Table captions and th scope="col"
- prefers-reduced-motion support
- Layout works down to small phone widths without sideways page scroll


---------------------------------------------------------------------
6. CONTENT TO CONFIRM BEFORE SUBMISSION OR PUBLICATION
---------------------------------------------------------------------
Much of the text is sample content and must be confirmed with the
school:
- School address, telephone numbers, email addresses, opening hours
- Statistics (pass rate, number of learners, staff, teacher ratio)
- Fees, key dates and intake wording (add years to term dates)
- Names of staff and the Head Teacher's message
- The list of services shown on services.html

Files that must exist (or paths must be changed):
- All images in images/ (each below 200 KB)
- media/school-introduction.mp4 and school-introduction-en.vtt
- media/drama-club.mp4 and drama-club.webm


---------------------------------------------------------------------
7. KNOWN LIMITATIONS AND SUGGESTED FIXES
---------------------------------------------------------------------
- Forms use action="#" and method="post": they validate in the browser
  but do not send data. Connect them to a server script or form service
  and add server-side validation before going live.
- --ink-muted (#6c7a90) is about 4.35:1 on white, below the 4.5:1
  minimum. Darken it (for example #5b6a80).
- .container is capped at 1100px by an older max-width rule even though
  --content-width is 1180px. Keep only one of the two values.
- The reduced-motion rules shorten transitions but cards and buttons
  still shift on hover. Add:
      @media (prefers-reduced-motion: reduce) {
        .card:hover, .btn:hover, .mini-form button:hover {
          transform: none; box-shadow: none;
        }
      }
- .staff-table is a leftover class name; it styles all tables. Consider
  renaming it to .data-table.
- Search all ten files for links to removed pages (staff.html,
  news.html, downloads.html, curriculum.html, school-life.html).
- The header and footer are repeated by hand in every file; keep all
  ten copies identical when you edit.


---------------------------------------------------------------------
8. PRE-SUBMISSION CHECKLIST
---------------------------------------------------------------------
[ ] Every fact, number, name and fee confirmed with the school
[ ] Placeholder text, numbers and sample names replaced
[ ] Images compressed (below 200 KB each); video and .vtt file added
[ ] Every menu, footer and in-page link tested (no 404 errors)
[ ] Forms tested for required fields, email, phone, message length
[ ] W3C HTML and CSS validators run with no errors
[ ] Lighthouse or WAVE accessibility check run
[ ] Tested on at least one phone and one computer
[ ] Tested with "reduce motion" switched on
[ ] Folder structure matches section 2 of this file


---------------------------------------------------------------------
9. TECHNOLOGIES
---------------------------------------------------------------------
HTML5, CSS3 (custom properties, Flexbox, Grid, media queries).
OpenStreetMap iframe on the Contact page.


---------------------------------------------------------------------
10. CREDITS
---------------------------------------------------------------------
Prepared by:  [MUGERWA MARVIN AND MUKISA AVIN]
Reg. number:  [25/U/BIT/0032/K/WKD AND 26/U/BIT/0008/K/WKD]
Course unit:  [WEBSITE DEVELOPMENT /PROJECT]
Institution:  [MUTEESA 1 ROYAL UNIVERSITY]
Date:         [14/11/2026]
