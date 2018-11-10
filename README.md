# AU2018_AutodeskForgeNewB_Mod1_Postman

This tutorial/video is the first in the AU2018 NewB Launch, intended to help those interested in learning more about both coding and Forge.  I am a VDC Manager... not a programmer by trade... I am using an interest in Forge to push myself to learn to code and am sharing with you so you can learn it too.  Hopefully hearing from this NewB perspective will bring value to you.

This module is based on a Youtube video that helped me get started.  Rather quickly you can get a working model in a simple locally run website.  It also helped me to see and understand the administrative steps that we will later automate somewhat.  Seeing these steps will help you know when something is not working right and which step is probably the issue.  

Module 1 introduces you to the steps that are required to:

- Create an Autodesk Forge app
- Pull an access token
- Create a bucket
- Upload a file
- Translate that file to SVF
- Track the progress of the file translation
- Update a simple index.html (which will load the model viewer and the model)
- View the model in Chrome

Key learnings:
- What is a client key and secret and how can they be used to retrieve an access token
- You must get an access token to access your app (this is for your own protection so that if someone
- You must create a bucket, then upload one of 60 file formats into the bucket 
- That file must be "Translated" in order to be viewed in the Forge web platform, we will translate to SVF format
- The translated file is given a URN (essentially the systems filename for this newly translated file)
- The access token and URN can be used in the simple HTML file to acces the viewer and view the uploaded file in a web browser 

Important Notes:
- Make sure that you set the    "compressedUrn": false,     if you are NOT uploading a zip file.  If you are set to true
- Understand that your access token is only good for 3600 seconds after that it will expire and will not be useable anylonger to continue viewing 
the model in your HTML after that timeframe you will need to retreive a new access token and then copy and paste it into the HTML again.
- A bucket can only be created once and must have a unique name in the format of xxxxxxx_xxxxxxx (at least that is all that has worked for me) if you need to create a bucket again you will need to adjust the value set in the environment variables in postman otherwise you will get an error.

This has been writen by a fairly inexperienced NewB for other NewBs.  Hopefully going throuhg this introduction will help you.

Our next step will be to build a website based on the learn.forge.io that will allow you to do the uploading/translating/vieweing directly from there.

This is based on a video by THEASKERSLAB found here: https://www.youtube.com/watch?v=6O4Td3F4IjA&t=327s on youtube...
many thanks for your video.  It is only being remade here as a part of a tutorial series.

Forge.Viewer.Classroom.Trainning-master is from JohnOnSoftware https://github.com/JohnOnSoftware/Forge.Viewer.Classroom.Trainning

MyPostmanCollections-master is from adamenagy https://github.com/adamenagy/MyPostmanCollections

