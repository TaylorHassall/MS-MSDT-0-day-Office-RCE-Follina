# MS-MSDT-0-day-Office-RCE-Follina
Pre-Created document xml files for creating the Documents required for PoC MSDT Follina

**Big Thanks to https://gist.github.com/tothi from whom this information comes from. I just re-wrote it for myself. Please give all praise to Tothi (https://twitter.com/an0n_r0)**

**Using pre-created xml file process**
DOCX Creation

0. Open Document.xml.rels and replace "Target="XXXXXXXXXXXXXXXXXXXXX.html!" with your hosted remote doc.
1. Create a Docx file.
2. In the Docx file, Insert > Object > Bitmap Image > Ok
3. In the Paint application that launched, put in whatever you would like, or leave blank. Save the Paint file.
4. Save your Docx file.
5. Open your file as an archive (With 7Zip; Right Click > 7Zip > Open Archive.)
6. In the 7Zip prompt, open the \Word Folder, and replace the Document.xml with the Document.xml downloaded from this POC. Then navigate to \word\_rels\ and replace the document.xml.rels file with the one downloaded from this POC.
7. Launch the Docx file.

**DIY**
1. Create a Docx file.
2. In the Docx file, Insert > Object > Bitmap Image > Ok
3. In the Paint application that launched, put in whatever you would like, or leave blank. Save the Paint file.
4. Save your Docx file.
5. Open your file as an archive (With 7Zip; Right Click > 7Zip > Open Archive.)
6. Copy out the Document.xml from \Word\ and document.xml.rels file from \word\_rels\
7. Open/Edit the Document.xml.rels and locate the relationship XML Tag with "/relationships/oleObject". After this replace the destination in "Target=" to your remote destination where it will grab the payload from. Also add "TargetMode="External"" to the XML Tag. 
![image](https://user-images.githubusercontent.com/79787840/171080197-9c253852-a5c5-4df2-a6be-63a6165f86e5.png)
8. Open/Edit the Document.xml and locate the "o:OLEObject" tag. Change "Type="Embed" to "Type="Link" and add "UpdateMode="Oncall"
![image](https://user-images.githubusercontent.com/79787840/171080503-f427ae2d-c8d8-42bb-89b7-46d3b3d1f098.png)
9. Upload your remote HTML file to the destination in step 7.
10. Launch the Docx file.
