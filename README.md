# html-based-epub-experimental
This is a provisional sample of an HTML-based EPUB (in Japanese), created for testing purposes based on https://github.com/w3c/epub-specs/pull/2709, which explores the HTML serialization of EPUB 3.

* Originai XHTML-Based EPUB3
  * Chemical-History-of-a-Candle
* Converted HTML- Based EPUB3
  * Chemical-History-of-a-Candle-html-based

## What was changed?
* OPF
  * Changed file extensions from .xhtml to .html and updated the media-type from application/xhtml+xml to text/html.
  * Removed ncx from the manifest, and also removed toc="ncx".
  * The OPF file itself remains in XML format (not XHTML), so no format change was made.
* XHTML
  * Changed file extensions from .xhtml to .html.
  * Removed <code>&lt;?xml version="1.0" encoding="utf-8"?&gt;</code>.
  * Changed <code>&lt;html xmlns="http://www.w3.org/1999/xhtml" xmlns:epub="http://www.idpf.org/2007/ops" xml:lang="ja"&gt;</code> to <code>&lt;html lang="ja"&gt;</code>.
  * Replaced all <code>/&gt;</code> with <code>&gt;</code>.
  * Changed <code>epub:type</code> to <code>epub-type</code>.

## EPUBCheck v5.2.1 Results
~~~
Validating using EPUB version 3.3 rules.
ERROR(OPF-012): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(20,78): Item property "nav" is not defined for media type "text/html".
ERROR(OPF-012): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(21,95): Item property "svg" is not defined for media type "text/html".
ERROR(RSC-005): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(20,78): Error while parsing file: The manifest item representing the Navigation Document must be of the "application/xhtml+xml" type (given type was "text/html")
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(21,95): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(22,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(23,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(24,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(25,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(26,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(27,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(28,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(29,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(30,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(31,78): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(OPF-043): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(41,90): Spine item with non-standard media-type "text/html" has no fallback.
ERROR(CHK-008): /home/koike/git/html-based-epub-experimental/Chemical-History-of-a-Candle-html-based.epub/OEBPS/Chemical-History-of-a-Candle.opf(-1,-1): Error encountered while processing an item "OEBPS/toc.html"; skip other checks for the item.

Check finished with errors
Messages: 0 fatals / 16 errors / 0 warnings / 0 infos

EPUBCheck completed
~~~