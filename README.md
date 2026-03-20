# Host-a-Static-Website-on-AWS-S3-CloudFront-

What you’ll build

A live website (HTML/CSS) hosted using:

Amazon S3 (storage)

Amazon CloudFront (fast global delivery)

🪜 Step-by-Step Guide
✅ Step 1: Create a simple website

On your computer:

Create a folder my-website

Inside it, create a file index.html

Example:

<!DOCTYPE html>
<html>
<head>
  <title>My AWS Website</title>
</head>
<body>
  <h1>Hello from AWS 🚀</h1>
  <p>This is my first cloud project.</p>
</body>
</html>
✅ Step 2: Create an S3 Bucket

Go to AWS Console

Search for S3

Click Create bucket

Give a unique name (e.g., my-aws-site-12345)

Choose region (closest: Mumbai)

Uncheck "Block all public access"

Create bucket

✅ Step 3: Upload Website Files

Open your bucket

Click Upload

Add your index.html

Click Upload

✅ Step 4: Enable Static Website Hosting

Go to Properties tab

Scroll to Static website hosting

Enable it

Enter:

Index document: index.html

Save

👉 You’ll get a Bucket Website URL

✅ Step 5: Make Files Public

Go to Permissions tab

Add bucket policy:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::YOUR-BUCKET-NAME/*"]
    }
  ]
}

Replace YOUR-BUCKET-NAME

✅ Step 6: Access Your Website

Open the S3 website URL in browser 🎉
Your site is now live!
