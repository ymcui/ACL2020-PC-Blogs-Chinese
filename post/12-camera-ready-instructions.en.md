# Camera Ready Instructions
(These instructions are adapted from ACL 2019). 

### When and where do I send my final camera-ready paper?

The deadline is May 1 (at 11:59pm, UTC-12 hours, “anywhere on Earth”). You may submit the final version of your paper by navigating to the [ACL 2020 START login](https://www.softconf.com/acl2020/papers/) and following the internal links.

### How should I enter metadata on the START system?

The metadata (title, author, abstract) that you enter into START is very important, because it is used on the conference website, handbook, mobile app, and the [ACL Anthology](http://www.aclweb.org/anthology/) (and propagates to Google Scholar, etc).

Before the metadata is entered, please have all authors ensure that the name in their START profile (User Console, Update Profile) appears exactly the way that they want it to appear. <br/>
- Unicode (UTF-8) can be used for accented or special characters.
- Ordinarily, names are <b>not</b> written in all caps or all lowercase.
- The "Last Name" is the name(s) by which your paper is to be cited. It is usually a family name, even for authors from cultures where the family name is written first.
- The "First Name" is usually a given name or names, including middle names/initials.

The metadata should be written using Unicode (UTF-8) with LaTeX commands. Please try to follow these guidelines: <br/>
- In titles, please capitalize the first word, the first word after a colon (:), and all other words except the following “little words”: articles, prepositions, coordinating conjunctions, and the infinitive marker “to.” This includes hyphenated words like Mixed-Case.
- BibTeX (in many bibliography styles, including ACL's) lowercases the titles of conference papers, and needs to be told which letters not to lowercase. So if your title has letters that should always be capitals, please protect them with curly braces, like this: <i>{E}nglish, {C}homsky, {IBM}, {CFG}s, {HMM}s</i>. Please also protect the first letter after a sentence-final punctuation mark. For example: <i>Can {LSTM} {L}earn to {C}apture {A}greement? {T}he {C}ase of {B}asque Named {E}ntity {E}xtraction from {N}oisy {I}nput: {S}peech and {OCR}</i>. These curly braces will _not_ appear in the online conference program or proceedings. They will only appear in the BibTeX file that others will use to cite your paper.
- If you need literal curly braces, please escape them like this: \{ \}
- Please don't use any nonstandard LaTeX commands, and there should be no \footnote or citations using \cite or related commands.
- You can use LaTeX math mode where appropriate: An $O(n^2)$ Algorithm for $n$-gram Smoothing.
- You can use Unicode (UTF-8) for accented or special characters.
- If you copy-and-paste from your PDF file, please be sure to rejoin words broken by hyphenation.

### How should the final copy differ from the original submission?

The camera-ready version of your paper should incorporate the comments of the reviewers as well as other changes you see fit to make. In addition, be sure to do all of the following: <br/>
- Ensure that your paper conforms to the [provided styles, font and page size](https://acl2020.org/calls/papers/).
- Include the authors' names and affiliations under the title. Note that the list of authors should be identical to the list specified when submitting the paper. 
- De-anonymize references to your own work in the body of the paper.
- Where appropriate, add acknowledgments for colleagues, reviewers, and grants. Do not number the Acknowledgements section. Please note that the acknowledgement section should fit within the allowed page limits (9 pages of content for long papers, 5 pages of content for short papers) and be in the same font as the rest of the paper.
- Ensure that all tables, graphs, and figures are readable at standard resolutions.
- If you have supplemental material (including written material, data, and/or code) ensure that all the components are put at the right place (more on that below).

### What are the tips to make my final version more accessible? 

As a central venue of publication for our community, please prioritise the accessibility of your final version.  The Diversity & Inclusion committee for ACL2020 has outlined some tips on how to do this: [https://acl2020.org/blog/accessibility-for-camera-ready/](https://acl2020.org/blog/accessibility-for-camera-ready/)

### Where do appendices and supplemental material go?

Supplemental material can be divided into two types: appendices and non-readable supplemental material. <br/>
- Appendices are material that can be read, and include lemmas, formulas, proofs, and tables that are not critical to the reading and understanding of the paper. In your final camera-ready paper, appendices come after the references in the main paper and use the same two-column format as the rest of the paper (see the ACL 2020 style files for an example). Appendices do not count towards the page limit.
- Non-readable supplemental material (data, software, all other material) is uploaded separately.

### How long can it be?

Long papers are permitted at most 9 pages of text while short papers may use up to 5 pages of text. Please use the extra space to help address reviewer comments. For both long and short papers, there is no page limit for references or appendices.

### What is the format for the camera-ready copy?

The file must be in Portable Document Format (PDF) on A4 paper. We require the use of [ACL LaTeX style files or Microsoft Word Style files tailored for this year's ACL conference](http://acl2020.org/downloads/acl2020-templates.zip). You can view the style files and detailed formatting instructions on the web.

If you are using LaTeX, please create the PDF file with pdflatex or xelatex. This ensures use of the proper Type 1 fonts and also takes advantage of other PDF features. You will have the best results using a modern LaTeX distribution, in particular, [TeX live](http://www.tug.org/texlive/). Using the geometry package to set the A4 format is recommended.

### How do I ensure that my file is correctly formatted?

<b>Checking the paper size.</b> Your paper needs to be formatted to A4. Here are a couple of ways to check this:<br/>
- Using pdfinfo. The `pdfinfo` command should include “Page size: 595.276 x 841.89 pts” in its output.
- Using Apple's Preview.app. Open the PDF, and type Ctrl-I. It should report the correct page size.
- Using Adobe Acrobat. Open the PDF, navigate to File, Properties..., Description. The field labeled "Page Size" should read 8.27 × 11.69 inches in.

<b>Embedding Fonts.</b>  You can check your final PDF with the command pdffonts mypaper.pdf and confirm that all the fonts say "yes" under "emb". START will not let you upload your final PDF otherwise. If you are including graphics with the PDF extension, these files must also have embedded fonts. If your paper uses Asian fonts, they must be embedded in the PDF file so that they can be displayed by non-Asian versions of the PDF reader (Asian versions ship with a larger set of default fonts.) 

### What if my paper includes graphics?

Remember that you are providing a camera-ready copy. Thus, artwork and photos should be included directly in the paper in their final positions. Ideally, you should use vector graphic formats (PDF, EPS), which allow the graphics to scale arbitrarily. Avoid GIF or JPEG images that are low resolution or highly compressed.

Your paper must look good both when printed (A4 size) and when viewed on screen as PDF (zoomable to any size, color okay). Thus, you may want to use color high-resolution graphics, allowing readers to zoom in on a graph and study it. However, please check that the same graph or photograph is legible when printed and in a PDF viewer at different resolutions.
Don't go overboard on resolution; keep file sizes manageable. Note that vector graphics (e.g., encapsulated PostScript) look good at any scale and take up little space (unless you are plotting many thousands of data points).

### What about copyright?

When you submit the paper, you will be asked to sign the ACL Copyright Transfer Agreement on behalf of all authors, either electronically (via the [START Conference Manager](https://www.softconf.com/acl2020/papers/)) or physically. Authors retain many rights under this agreement and it is appropriate in the vast majority of cases. Please contact the publication chairs Douwe Kiela and Ivan Vulić with any concerns regarding copyright.

Before signing this form, please confirm with your co-authors (and, if applicable, your and their employers) that they authorize you to sign on their behalf. Please sign your full name (not just your first or last initials).

### What if my paper's title or other metadata has changed?

Then please edit those metadata fields when you upload the camera-ready version, so that they will appear correctly in the table of contents, author index, conference schedule, etc.

Please also note that your name will appear in conference metadata as you have configured it in START, so make sure that it is correct there (e.g., capitalization, full name, etc). You can change this on the [user settings](https://www.softconf.com/acl2020/super/scmd.cgi?ucmd=updateProfile) page of the START conference manager, under "User" > "Account Information" > "Update Profile".

### My question isn't answered here…

Please email the publication chairs [Steven Bethard](https://bethard.faculty.arizona.edu/), [Ryan Cotterell](https://ryancotterell.github.io/), and [Rui Yan](http://www.ruiyan.me/). 
