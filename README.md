# Digital Asset Manager Figma Widget
<!-- 
  Do not edit directly, built using contentful-readme-generator.
  Content details in Build Information below.
-->

- [Digital Asset Manager](#digital-asset-manager)
- [Attaching to Figma Node](#attaching-to-figma-node)
- [Contentful Settings](#contentful-settings)
- [Contentful Management Token](#contentful-management-token)
- [Custom Contentful "Image" Content Type](#custom-contentful-image-content-type)
- [Publishing and Reconnecting to Contentful](#publishing-and-reconnecting-to-contentful)
- [Build Information](#build-information)

---


__Project Abbreviation__: DAM

__Developer Emails__: scott.rouse@gmail.com

__Production URL__: https://digitalassetmanager.app

## Digital Asset Manager
The Digital Asset Manager widget solves the problem of lost source files by binding your Figma images directly to your Contentful space ( https://contentful.com ). The widget is presently in closed release, but will be published in the coming months.

[![Digital Asset Manager](https://images.ctfassets.net/rtkhko6y3s3u/13jGhOwlo0muEynR9bm8tU/d979bc587e7069f28ad3f02cf02579a7/Digital_Asset_Manager.png)](https://images.ctfassets.net/rtkhko6y3s3u/13jGhOwlo0muEynR9bm8tU/d979bc587e7069f28ad3f02cf02579a7/Digital_Asset_Manager.png "View Full Size")
    
Digital Asset Manager, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/21ux5cSS1qYPZEfRasDPVY), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=303:327)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/2WANSGlMSfYfALvZCVqLBe)

## Attaching to Figma Node
To attach a Figma image to the widget, drag and drop a new widget (or copy existing widget) onto the stage, open the widget's configuration window (via the "i" information button), select your target Figma node, and hit "Attach". The widget will automatically snap to the top left corner of your Figma graphic.

If you already have a DAM widget on stage that is configured to Contentful, a copy/paste of that widget will sustain the configurations.

[![Attaching to Figma Node](https://images.ctfassets.net/rtkhko6y3s3u/eGhXgjwUw9sSQMWHGK8dQ/bcfbb5309207162b83a05b36e8210ffe/Attaching_to_Figma_Node.png)](https://images.ctfassets.net/rtkhko6y3s3u/eGhXgjwUw9sSQMWHGK8dQ/bcfbb5309207162b83a05b36e8210ffe/Attaching_to_Figma_Node.png "View Full Size")
    
Attaching to Figma Node, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/5nKkocYVSlEQvGg3Zsul5J), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=305:531)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/4w5CuyVObSz1p5uqLQdGwO)

## Contentful Settings
To connect your Figma widget to Contentful, you will need to enter the space id and a CMA (Contentful Management API - details below) access key. After you have entered both, then select the deployment environments. The widget will cycle through each of these selected environments when deploying.

[![Contentful Settings](https://images.ctfassets.net/rtkhko6y3s3u/6cf7M0XwQkt8bnH7vcKaHL/c478f83c166b60b134203de9e76e36c3/Contentful_Settings.png)](https://images.ctfassets.net/rtkhko6y3s3u/6cf7M0XwQkt8bnH7vcKaHL/c478f83c166b60b134203de9e76e36c3/Contentful_Settings.png "View Full Size")
    
Contentful Settings, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/aRn4y93qzxIh9lRROaBa5), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=303:353)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/7pSimTv5Bu3vgCOAO4hrSB)

## Contentful Management Token
The Contentful Management Token is created within the APIs section of your Contentful space. This token will enable the widget to create and update entries in your Contentful space.

[![Contentful Management Token](https://images.ctfassets.net/rtkhko6y3s3u/6Nv7tZ6X8kMehE8yrl74yf/5234ff9e9621fb0568e9667dfc03e45d/Contentful_Management_Token.png)](https://images.ctfassets.net/rtkhko6y3s3u/6Nv7tZ6X8kMehE8yrl74yf/5234ff9e9621fb0568e9667dfc03e45d/Contentful_Management_Token.png "View Full Size")
    
Contentful Management Token, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/5FeS5fPlM4YB89FPF1H4x6), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=304:407)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/60zkRVYOpKZvnW1gAM0O9B)

## Custom Contentful "Image" Content Type
In order for the Digital Asset Manager to stay synced between Figma and Contentful, some metadata has to be stored on both sides. Within Figma this stays within the widget, but for Contentful you will need to create a special content type that can store this extra information. This content type minimally requires an "asset" property pointing to media and a "digitalAssetManagerId" property, but in order to easily link back to Figma it is highly recommended to also add the properties of "figmaFileId" and "figmaNodeId". If you decide to use a different name for this content type than "image", you can set that in the Figma widget settings.

[![Contentful Image Content Type](https://images.ctfassets.net/rtkhko6y3s3u/2fM3WUg2uVVlKJ0m1Do3qI/b81f3a53b80a61c8d1064a5282d671e6/Contentful_Image_Content_Type.png)](https://images.ctfassets.net/rtkhko6y3s3u/2fM3WUg2uVVlKJ0m1Do3qI/b81f3a53b80a61c8d1064a5282d671e6/Contentful_Image_Content_Type.png "View Full Size")
    
Contentful Image Content Type, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/rYxRVsNbcewbVCRZ5D86B), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=303:503)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/CnUN959efto8MDwlyJJsj)

## Publishing and Reconnecting to Contentful
If everything is set up correctly, publishing is just one click. With that click the new image will be pushed to Contentful and the original entity's asset will be replaced with the new image.

If you have accidentally deleted the Figma asset, you can reconnect a new DAM widget to the Contentful entity by copy/pasting the digital asset manager id found in Contentful into the settings of the new widget.

[![Publishing to Contentful](https://images.ctfassets.net/rtkhko6y3s3u/2RokQ0mSF7abpK6qqrvkH1/ae676eaa3f046529b2343edc1fa8b49d/Publishing_to_Contentful.png)](https://images.ctfassets.net/rtkhko6y3s3u/2RokQ0mSF7abpK6qqrvkH1/ae676eaa3f046529b2343edc1fa8b49d/Publishing_to_Contentful.png "View Full Size")
    
Publishing to Contentful, source: [contentful](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/21DCxaROOsa8fWjEfvKggJ), [figma](https://www.figma.com/file/fdgg22P6rDRQl3rDWl7RHs/?node-id=303:446)


[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/39TrkSGTlNqcW27DCcet33)

## Build Information

*Dynamically built using contentful-readme-generator. Do not edit directly.*

*__updated__: 3/19/2023, 5:22:24 PM*

*__space__: rtkhko6y3s3u*

*__environment__: master*

*__entity id__: 2CUvXYgc2NR1L6069579nB*

[&#9998; edit](https://app.contentful.com/spaces/rtkhko6y3s3u/environments/master/entries/2CUvXYgc2NR1L6069579nB)
