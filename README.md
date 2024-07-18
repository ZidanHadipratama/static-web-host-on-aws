# Static Web Hosting Project on AWS using AWS S3

First I add the bucket in my AWS S3 with this configuration :

![alt text](image.png)

![alt text](image-1.png)

![alt text](1-aws-p1.png) 

I set `ACLs enabled` so I can have full access of the permission on files.

I also uncheck the `Block Public Access settings for this bucket` so public can have access to my file.

And then I upload the file that are needed for the page. 

![alt text](2-aws-p1.png) 

Index.html is the website, and the zip files containe all the resources that are related to the website. 

Then I setup the index.html so it's can be accessed by anyone who click the link.

![alt text](4-aws-p1.png) 

![alt text](3-aws-p1.png) 

But, when we click the page. it's give this output:

![alt text](5-aws-p1.png) 

This error because I didn't set the right permission for my file.

So now this is the way to fix it. Click the file, go to `permission` tab and then set this configuration:

![alt text](image-2.png)

After that, the website is accessible?:

![alt text](6-aws-p1.png)

Well, not quite. So, my problem is I input the zip files, not the folder and didn't set the permission on the folder.

So, to set the entire folder to right permission, I block the folder, and go to `Actions` and then `Make Public using ACLs`.

This is the output when I success set the folder to public:

![alt text](image-3.png)

Now let's try to access the website again if it's working:

![alt text](7-aws-p1.png)