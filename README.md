# Host-a-Website-on-Amazon-S3
In this project, I will demonstrate how to host a static website on Amazon S3. I'm doing this project to learn base of how things work in the cloud. 
### Tools and concepts

Services I used were amazon s3,  Key concepts I learnt include include bucket policy, bucket end point url, html, static website hosting, acl and how they control acess to our bucket objects. 

### Time, challenges, and wins

This project took me approximately 1:30 . The most challenging part was resoving the 403 error at all It was most rewarding to see my statitc website being live to the world. 

---

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will create an account and create a storage space for my website I use the free piere version of AWS because it is a simple first project . 

### How long it took to create the bucket

Creating an S3 bucket took me  less than 5 min. 

### Region selection

The Region I picked for my S3 bucket was Oregon because live in seattle and it is the closest distance for me . 

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means that no other s3 bucket in the whole word can have that same.regarless of zone and region. 

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_ba6d42ad)

---

## Upload Website Files to S3

### What I did in this step

In this step, I will upload S3 files  because our buket is still empty. so that we have a website to host . 

### Files I uploaded

I uploaded two files to my S3 bucket - they were one index. html file and the other is folder with files and images. 

### How the files work together

Both files are necessary for this project as index. html is the one that defines the  structure  and the files are the contents of the website. i.e if index.html says interest image here it might not have the image to supply so that is why we have multiple files uploaded . Index.html is to show what is in the the website and the files are the contents.

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_a265af88)

---

## Static Website Hosting on S3

### What I did in this step

In this step, I will make my website avaliable  to the world because it is called static web hosting .

### Understanding website hosting

Website hosting means Putting website files on a webserver which is a computer designed turn the files into the websites pages that people can visit. 

### How I enabled website hosting

To enable website hosting with my S3 bucket, I went to the properties tab and enables static webhosting and named the file as index.html. 

### Access Control Lists (ACLs)

An ACL is a way to congure permission setting to controll acess. . we enabled it to control access to our website files later. There was a pop up that aws reccomend that AWS to be disabled but we enabled it learn and compare it with buvket polices. 

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_c22c54c0)

---

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is url that takes you to the website . 

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I saw saw an 403 error cause objects in bucket are public by default even tho we switched of lock up public acess the website files are still completly private. we need to manage the acess setting separetly. They need to be public files to for the public to see the content of out website. 

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_22ce4daf)

---

## Success!

### What I did in this step

In this step, I will go the files I uploaded because it will enables us to see the content of the website . once that is done our website is officaly done. 

### How I resolved the 403 error

To resolve this 403 Forbidden error, I went to objects , then select both the file and folder then update the ACL bucket files public. Once we checked our  s3 bucket endpoint we can see a webpage all loaded up. 

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_5d4474f9)

---

## Bucket Policies

### What I did in this extension

In this project extension I'm about toput  bucket policy  I'm doing this so that others cant not delete my index. html. 

### Understanding bucket policies

An alternative to ACLs are bucket policies, which arerules The benefit of using bucket policies is even greater control of the access of the actions that people are or are not allowed to do.  while ACLs are useful for public access for individual objects. 

![Image](http://nextwork.ai/loving_gold_playful_ruru/uploads/aws-host-a-website-on-s3_sm2sm2sm)

### What my bucket policy does

My bucket policy denies everyone from deleting our index. html file. I tested this by tying to delete index. html and saw permission denied which means our bucket policy succefully worked. 

---

---
