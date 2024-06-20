Font squirrel:
https://www.fontsquirrel.com/

Web font generator:

https://www.fontsquirrel.com/tools/webfont-generator


Let's find some fonts! Go to Font Squirrel and choose two fonts: a nice interesting font for the headings (maybe a nice display or slab serif font), and a slightly less flashy and more readable font for the paragraphs. When you've found a font, press the download button and save the file inside the same directory as the HTML and CSS files you saved earlier. It doesn't matter whether they are TTF (True Type Fonts) or OTF (Open Type Fonts).

Unzip the two font packages (Web fonts are usually distributed in ZIP files containing the font file(s) and licensing information). You may find multiple font files in the package — some fonts are distributed as a family with different variants available, for example thin, medium, bold, italic, thin italic, etc. For this example, we just want you to concern yourself with a single font file for each choice.

Note: In Font Squirrel, under the "Find fonts" section in the right-hand column, you can click on the different tags and classifications to filter the displayed choices.

Generating the required code
Now you'll need to generate the required code (and font formats). For each font, follow these steps:

1. Make sure you have satisfied any licensing requirement if you are going to use this in a commercial and/or Web project.

2. Go to the Fontsquirrel Webfont Generator.

3. Upload your two font files using the Upload Fonts button.

4. Check the checkbox labeled "Yes, the fonts I'm uploading are legally eligible for web embedding."

5. Click Download your kit.

After the generator has finished processing, you should get a ZIP file to download. Save it in the same directory as your HTML and CSS.



## Implementing the code in your demo


At this point, unzip the webfont kit you just generated. Inside the unzipped directory you'll see some useful items:

Two versions of each font: the .woff, .woff2 files.
A demo HTML file for each font — load these in your browser to see what the font will look like in different usage contexts.
A stylesheet.css file, which contains the generated @font-face code you'll need.
To implement these fonts in your demo, follow these steps:

Rename the unzipped directory to something easy and simple, like fonts.
Open up the stylesheet.css file and copy the two @font-face rulesets into your web-font-start.css file — you need to put them at the very top, before any of your CSS, as the fonts need to be imported before you can use them on your site.
Each of the url() functions points to a font file that we want to import into our CSS. We need to make sure the paths to the files are correct, so add fonts/ to the start of each path (adjust as necessary).
Now you can use these fonts in your font stacks, just like any web safe or default system font. For example:
CSS
Copy to Clipboard
@font-face {
  font-family: "zantrokeregular";
  src:
    url("fonts/zantroke-webfont.woff2") format("woff2"),
    url("fonts/zantroke-webfont.woff") format("woff");
  font-weight: normal;
  font-style: normal;
}
CSS
Copy to Clipboard
font-family: "zantrokeregular", serif;