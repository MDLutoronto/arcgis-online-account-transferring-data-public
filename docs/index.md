---
title: "Transferring Data to a Public ArcGIS Online Account"
layout: "home"
description: "This tutorial provides step-by-step guidance on how to transfer work on ArcGIS Online from a University of Toronto (UofT) institutional account to the free (aka ‘public’) version of the service."
permalink: "/"  #! Remove this if not the homepage
---

# Transferring Data to a Public ArcGIS Online Account

This tutorial provides step\-by\-step guidance on how to transfer work on ArcGIS Online from a University of Toronto (UofT) institutional account to the free (aka ‘public’) version of the service.

Due to the [University of Toronto ArcGIS Online Data Retention Policy](https://mdl.library.utoronto.ca/technology/gis-software/arcgis-online-data-retention-policy) (effective January 1, 2024\), the Map & Data Library now conducts data cleanups on a regular basis. As part of this process, UofT user accounts that have not been accessed for over 12 months may be deleted, along with all associated content (e.g., datasets, maps, apps).

To support the long\-term preservation of ArcGIS projects for individuals who are no longer affiliated with the university, this tutorial is intended to assist UofT students, faculty, and staff in transferring and storing work in a personal (public) account.

### **Tables of Contents**

[Transferable Items](#transferable-items)  
[Exporting Tools](#exporting-tools)  
[Tool Limitations](#tool-limitations)  
[Format Considerations](#format-considerations)  
[Exporting Data from Item Page](#exporting-data-from-item-page)  
[Exporting Data using Extra Data tool](#exporting-data-using-extra-data-tool)  
[Uploading Data to Public Account](#uploading-data-to-public-account)  
[Learning More](#learning-more)  
 

## Transferable Items

To transfer data from an institutional ArcGIS Online account to a public (free) account, you can export only those layers that you own or that have export permissions enabled.

More complex items (e.g. web maps, StoryMaps) **cannot** be exported in full. To transfer these, you will need to manually download the individual assets (e.g., spatial layers, images, audio files) and recreate the item in your public account.

If you need assistance transferring a StoryMap or Instant App to your public account, please contact us using the [support form](https://mdl.library.utoronto.ca/about/contact). Note that certain applications (e.g. Experience Builder, Dashboards, Survey123\) are **not** supported in public accounts.

## Exporting Tools

We will cover two exporting tools in this tutorial: ***Export Data*** function on an individual item’s Details page and the ***Extract Data*** tool.

**Export Data** is a feature on the Item Details page in ArcGIS Online that allows users to export data in various formats, including Shapefile, CSV, KML, Excel, File Geodatabase (FGDB), GeoJSON, and GeoPackage. Only **hosted feature layers** can be exported. To learn more about the definition, see [feature layers](https://doc.arcgis.com/en/arcgis-online/reference/feature-layers.htm). For detailed instructions, see [ArcGIS Online: Export data from hosted feature layers](https://doc.arcgis.com/en/arcgis-online/manage-data/use-hosted-layers.htm#GUID-47A1D795-B330-45D7-89F7-9203A99E6924).

**Extract Data** tool is a geoprocessing tool in ArcGIS Online that packages feature layers and tables into formats such as CSV, File Geodatabase (.zip), Shapefile (.zip), and KML. This tool creates an item within your content that contains the data from the selected layers. You can download the data directly from the item. While powerful, the tool is applicable to layers that can be opened in **Map Viewer**. For detailed information on limitations, see the documentation [here](https://doc.arcgis.com/en/arcgis-online/analyze/extract-data-mv.htm).

## Tool Limitations

Exported files may take some time to process and might not be fully restorable in a public ArcGIS Online account. For the tools covered in this tutorial, please note the following common limitations:

* The time to export data from ArcGIS Online varies significantly depending on the size of the dataset, the internet connection, and the chosen export format. It can take anywhere from a few minutes to several hours, or even longer for large datasets.
* Some specialized layer types (e.g., raster layers, time\-enabled layers, or certain 3D layers) may not be compatible with both tools.

## Format Considerations

While ArcGIS Online supports a variety of export formats, public accounts only support uploading files in **CSV**, **KML**, and **GeoJSON** formats. When transferring data to a public ArcGIS Online account, it is important to understand the limitations of each supported file format:

* **GeoJSON**: Full feature properties (such as symbology and styles) may not be preserved during export/import. To maintain the same visual representation in the new map project, manual adjustments will be required after import.
* **KML**: While visible features are generally preserved, KML offers limited post\-import editing capabilities. For example, you will not be able to adjust styles or configure pop\-ups within ArcGIS Online after the import.
* **CSV**: Only non\-spatial attributes are retained unless the file includes latitude and longitude columns. Without spatial data, the CSV file cannot be imported as a spatial layer into a new map project.

## Exporting Data from Item Page

1. Log in to [ArcGIS Online](https://www.arcgis.com/sharing/oauth2/authorize?client_id=arcgisonline&response_type=code&state=%7B%22portalUrl%22%3A%22https%3A%2F%2Fwww.arcgis.com%22%2C%22uid%22%3A%22Eae4_LWCvrMN4HneelAeKdOsBBEPtvoRlAZMJG33ecw%22%2C%22useLandingPage%22%3Atrue%2C%22clientId%22%3A%22arcgisonline%22%7D&expiration=20160&locale=en-us&redirect_uri=https%3A%2F%2Fwww.arcgis.com%2Fhome%2Faccountswitcher-callback.html&force_login=true&redirectToUserOrgUrl=true&code_challenge=G5qu2wdtERhd8NB7wWeVriyIZeRVm6Aqu1YTsKbDJ64&code_challenge_method=S256&display=default&hideCancel=true&showSignupOption=true&canHandleCrossOrgSignIn=true&signuptype=esri&allow_verification=true) using organization’s URL and UTORid account (see instructions [here](https://mdl.library.utoronto.ca/technology/tutorials/logging-arcgis-online)).

2. Go to **Content** tab, navigate and click on the item in **Feature layer (hosted)** format.

    <img src='{{ '/assets/images/A2_DownloadingData_0.PNG' | relative_url }}' alt='Find feature layer (hosted) items in ArcGIS Online content' title='' width='261' height='198' />

 

3. On the layer's item details page, under the **Overview** tab, click **Export Data**, then **Export to GeoJSON**.

    <img src='{{ '/assets/images/A3.PNG' | relative_url }}' alt="Click 'Export Data', and then select 'Export to GeoJSON' from the dropdown" title='' width='353' height='554' />

4. Enter a title for the new file and add any other information. Then, click **Export**.

    <img src='{{ '/assets/images/A4_0.PNG' | relative_url }}' alt="Enter a name as the title, click 'Export'" title='' width='357' height='548' />

5. A new item page will open. On the **Overview** tab, click **Download** to save the file in the local computer.

    <img src='{{ '/assets/images/A5.PNG' | relative_url }}' alt="Click 'Download' under the Overview tab" title='' width='369' height='309' />  


 

## Exporting Data using Extra Data tool

1. Go to **Content** tab, navigate and click on a map itemto start.

2. Click **Open in Map Viewer**.

3. In the menu in the toolbar on the right, click **Analysis** icon, select **Extract Data** under **Manage data**.

    <img src='{{ '/assets/images/B3_Geoprocessing.PNG' | relative_url }}' alt="Find 'Extract Data' under 'Analysis' tab, and 'Manage data' category" title='' width='421' height='301' />

 

4. For **Input layer**, select the desired layer or layers. You can choose multiple layers here.

5. For the **Result layer**, specify the output data format, output name, and location.

    <img src='{{ '/assets/images/B5.png' | relative_url }}' alt='Setting parameters for the output' title='' width='365' height='351' />

 

6. Click **Estimate Credits** to check if you have enough credits. To view your remaining credits, click your **profile** in the top right corner, go to **My Settings**, and then select **Credits**. If you don’t have enough credits to run the tool, please contact the Map and Data Library using the [support form](https://mdl.library.utoronto.ca/about/contact-form).

7. Make sure you have enough credits, and click **Run**.

8. Go to **History** tab to check the processing statues and output.

    <img src='{{ '/assets/images/B8.PNG' | relative_url }}' alt="Geoprocessing statues is under 'History'" title='' width='380' height='151' />

 

9. Once the task is completed, click on the task record. In the open tab, click the three\-dot icon and select **Open Item Details**.

    <img src='{{ '/assets/images/B9.PNG' | relative_url }}' alt="In the open tab, click the three-dot icon next to the extracted item, then click 'Open item details'" title='' width='645' height='280' />

10. A new item page will open. On the **Overview** tab, click **Download** to save the file in the local computer.

    <img src='{{ '/assets/images/B10.PNG' | relative_url }}' alt="Click 'Download' under the Overview tab" title='' width='369' height='309' />

 

## Uploading Data to Public Account

1. If you don’t have an ArcGIS Online public account, use this [link](https://www.arcgis.com/sharing/rest/oauth2/signup?client_id=arcgisonline&redirect_uri=http://www.arcgis.com&response_type=token) to create one.

2. Log in to your [ArcGIS Online public account](https://www.arcgis.com/sharing/oauth2/authorize?client_id=arcgisonline&response_type=code&state=%7B%22portalUrl%22%3A%22https%3A%2F%2Fwww.arcgis.com%22%2C%22uid%22%3A%22Eae4_LWCvrMN4HneelAeKdOsBBEPtvoRlAZMJG33ecw%22%2C%22useLandingPage%22%3Atrue%2C%22clientId%22%3A%22arcgisonline%22%7D&expiration=20160&locale=en-us&redirect_uri=https%3A%2F%2Fwww.arcgis.com%2Fhome%2Faccountswitcher-callback.html&force_login=true&redirectToUserOrgUrl=true&code_challenge=G5qu2wdtERhd8NB7wWeVriyIZeRVm6Aqu1YTsKbDJ64&code_challenge_method=S256&display=default&hideCancel=true&showSignupOption=true&canHandleCrossOrgSignIn=true&signuptype=esri&allow_verification=true) using your ArcGIS login credentials.

    <img src='{{ '/assets/images/C2_ImportingData.PNG' | relative_url }}' alt='Login to public account using username and password' title='' width='377' height='526' />

 

3. Click on the **Map** tab to open the Map Viewer.

    <img src='{{ '/assets/images/C3.PNG' | relative_url }}' alt="Go to 'Map' from the top menu" title='' width='1311' height='312' />

 

4. Click **Add** from the left menu, select **Add layer from file**.

    <img src='{{ '/assets/images/C4.PNG' | relative_url }}' alt="Select 'Add' from the left toolbar, then select 'Add layer from file'" title='' width='443' height='247' />

 

5. Choose the file from your device, click **Open**, click **Create and add to map**.

    <img src='{{ '/assets/images/C5.png' | relative_url }}' alt='Open the exported file from your local device' title='' width='818' height='400' />

6. From the left menu, click **Save and open**, then **Save as**.

    <img src='{{ '/assets/images/C6_1.PNG' | relative_url }}' alt="Select 'Save and open' from the left toolbar, then select 'Save as'" title='' width='311' height='164' />

7. Fill out the title and click **Save**.

    <img src='{{ '/assets/images/C7_5.PNG' | relative_url }}' alt="Enter the name for the project, then click 'Save' to save the project" title='' width='404' height='421' />

8. The project is now successfully transferred and saved in your ArcGIS Online public account.

## Learning More

If you are interested in learning more about preserving GIS projects, transferring data from ArcGIS Online, or continuing your mapping projects using free GIS tools, consider exploring the following resources:

* The Map & Data Library offers [tutorials](https://mdl.library.utoronto.ca/support/tutorials-search) for [QGIS](https://qgis.org/), a free and open\-source GIS software available for everyone.
* You can [download publicly shared data in shapefile format](https://support.esri.com/en-us/knowledge-base/how-to-download-publicly-shared-data-from-arcgis-online-000015899) from ArcGIS Online to your local machine for use in other GIS platforms.
* Contact the Map & Data Library for further assistance at [mdl@library.utoronto.ca](mailto:mdl@library.utoronto.ca).

 

Technique: [Converting data formats](/technique/converting-data-formats), [Extracting data](/technique/extracting-data) \| Tools: [ArcGIS Online](/taxonomy/term/69)

**Date Created:** 2025\-05\-30 **Updated:** 2025\-05\-30
