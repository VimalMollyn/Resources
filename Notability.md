# Restoring Missing PDFs

If your PDF has disappeared from the background of your note, use the following steps to put the file back together. 

1. Export the .Note (with the missing background) and save it to your hard drive.
2. Edit the file name and change the extension from .Note to .Zip
3. Unzip that file and open up the resulting folder
4. Create a new folder and name it "PDFs"
5. Drag or paste the missing PDF into the newly named PDFs folder
6. Navigate back to the root level of the note and open up a folder named "NBPDFIndex"
7. Open the "NoteDocumentPDFMetadataIndex.plist" file
8. Copy the information in front of the .PDF up to the parenthesis. Your clipboard should contain a string of characters like so: FB544837-3C4B-4F70-A6D7-E7C9CB242E8C
8. Go back into the "PDFs" folder and rename the PDF with the pasted string
9. Navigate out of the file and compress the folder back into a .Zip file
10. Change the .Zip extension into a .Note, export to your iPad, and import into Notability

_Ref_: https://support.gingerlabs.com/hc/en-us/articles/360044382131-Restoring-Missing-PDFs
