# Google Docs Drawing Export
A few bookmarklets to help export higher (print) quality versions of Google Docs drawings.
 
## Setup
Add the following bookmarklets to your bookmarks toolbar (chrome and firefox).  You can do this by dragging the links below to the toolbar.

* [JQuerise](javascript%3A%28function%28%29%257Bif%28%21window.jQuery%29%257Bvar+script%3Ddocument.createElement%28%22script%22%29%3Bscript.src%3D%22%2F%2Fajax.googleapis.com%2Fajax%2Flibs%2Fjquery%2F1%2Fjquery.min.js%22%3Bdocument.head.appendChild%28script%29%3B%257D%257D%28%29%29): Adds jQuery to current page. (Needed for the following Bookmarklets)
* [Double Image Size](javascript%3A+var+imgs%3D%24%28%27img%5Bsrc%2A%3D%22google.com%2Fdrawings%2Fimage%3F%22%5D%27%29%3Bfor%28var+i%3D0%3Bi%3Cimgs.length%3B+i%2B%2B%29%7Bvar+img%3Dimgs%5Bi%5D%3Bvar+re+%3D+%2F%26h%3D%28%5B0-9%5D%2B%29%26w%3D%28%5B0-9%5D%2B%29%2F%3Bvar+m%3Bif%28%28m%3Dre.exec%28img.src%29%29%21%3D%3Dnull%29%7Bimg.src%3Dimg.src.replace%28re%2C%27%26h%3D%27%2B%28m%5B1%5D%2A2%29%2B%27%26w%3D%27%2B%28m%5B2%5D%2A2%29%29%3Bvoid%280%29%3B%7D%7D): Changes the url's for the GoogleDocs drawing images in current page to request one double the size.</li>
* [Download Links](javascript%3A+var+body+%3D+%24%28%27body%27%29%5B0%5D%3B+var+imgs+%3D+%24%28%27img%5Bsrc%2A%3D%22google.com%2Fdrawings%2Fimage%3F%22%5D%27%29%3B+for+%28var+i+%3D+0%3B+i+%3C+imgs.length%3B+i%2B%2B%29+%7B+var+img+%3D+imgs%5Bi%5D%3B+body.insertBefore%28%24%28%27%3Ca+href%3D%22%27+%2B+img.src+%2B+%27%22+download%3D%22drawing%27+%2B+%28i%2B1%29+%2B+%27.png%22%3Edrawing%27+%2B+%28i%2B1%29+%2B+%27.png%3C%2Fa%3E%3Cbr%2F%3E%27%29%5B0%5D%2C+body.children%5B0%5D%29%3B+void%280%29%3B%7D): Adds links at the top of the document for each drawing so you don't need to search through for all drawings

## Usage
1. Publish the document you wish to export.  From the **File** menu select **Publish to Web...**
2. Open **published version** of document
3. Click the **jQuerise** bookmarklet
4. Click the **Double Images Size** bookmarklet; once for 2x, twice for 4x etc.
5. Optionally, click the **Download Links** bookmarklet
6. Right-click on each drawing image and **Save image as** (OR right click on links at top to save link as)
