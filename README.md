# JQueryClientSideTranscript
This is a simple JQuery based example of calling the CSOD OData API

Please note that this will only run if hosted on the CSOD servers

Directions: 
  1. Go through the code and reference your own portal. (right now it is demopm.csod.com, change it to {yourportal}.csod.com)

#Hosting Files in Cornerstone

You can host files in Cornerstone with a workaround method using Course Publisher.

##How to Publish Files to Course Publisher

At a high-level, the steps are as follows:

1. Create an AICC compliant ZIP package which includes the files you would like to host.

2. Upload the ZIP file using Course Publisher, making note of the Publication ID

3. Construct the URL to the hosted file(s) using the generic URL format.

###Step 1 - Create an AICC compliant ZIP package which includes the files you would like to host.

1. There are four files which must be included in a ZIP file for it to be considered a compliant AICC package by Course Publisher:
  * CRS file
  * AU file
  * DES file
  * CST file

	We have provided a generic AICC package containing these four files which you can use for this purpose.

2. Place all files you would like to host in a single folder or folder tree.

3. Paste the four AICC files into the root of the folder containing the files you would like to host and create a ZIP file of the folder.

###Step 2 - Upload the ZIP file using Course Publisher, making note of the Publication ID

1. Upload the ZIP file using Course Publisher.
2. In Course Publisher, click on the title or edit icon of the publication you just created. Make note of the “publicatioId” value.

###Step 3 - Construct the URL to the hosted file(s) using the generic URL format.

1. The file can be referenced by inserting the Publication ID and appending the filename to the following URL: https://PORTAL_NAME.csod.com/content/PORTAL_NAME-NO_ENVIRONMENT/publications/PUBLICATION_ID/FILENAME.EXT

####Example 1

If the portal name is acme and in the PILOT environment, the file is “logo.swf”, and the publication ID = 123, then the link would be: http://acme-pilot.csod.com/content/acme/publications/123/logo.swf. Note there is “-pilot” for the first instance of PORTAL_NAME, however the second portal name instance does not reference the environment.

####Example 2

If the portal name is acme and in the PRODUCTION environment, the file is “logo.swf”, and the publication ID = 123, then the link would be: http://acme.csod.com/content/acme/publications/123/logo.swf.

##How to Update Published Files

You will need to delete the files you intend to update from the publication first, then load the new version.

1. In Course Publisher, find the Publication and click on the “Replace Publication Files” (the icon is a red and green arrow pointing in a circle).

2. Click the “Get Directory List” link under the DELETE FILES header.

3. Select the checkboxes next to the files you would like to update, then scroll to the bottom of the list and click “Delete”.

4. ZIP the updated file(s) into a ZIP file. Since you are “updating” a Publication, and not creating a new one, the ZIP file does not need to contain the four AICC files as it did when you first created the publication.

5. In Course Publisher, under the UPDATE FILES header, upload the new ZIP file using the Browse and Upload buttons. The new assets will then be loaded.
