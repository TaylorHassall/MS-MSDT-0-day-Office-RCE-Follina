# MS-MSDT-0-day-Office-RCE-Follina
Pre-Created document xml files for creating the Documents required for PoC MSDT Follina

DOCX Creation
0. Open Document.xml.rels and replace "Target="XXXXXXXXXXXXXXXXXXXXX.html!" with your hosted remote doc.
1. Create a Docx file.
2. In the Docx file, Insert > Object > Bitmap Image > Ok
3. In the Paint application that launched, put in whatever you would like, or leave blank. Save the Paint file.
4. Save your Docx file.
5. Open your file as an archive (With 7Zip; Right Click > 7Zip > Open Archive.
6. In the 7Zip prompt, open the Word Folder, and replace the Document.xml with the Document.xml downloaded from this POC. Then navigate to \word\_rels\ and replace the document.xml.rels file with the one downloaded from this POC.
7. Launch the Docx file.

