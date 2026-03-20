# Host-a-Static-Website-on-AWS-S3-CloudFront-

What you’ll build

A live website (HTML/CSS) hosted using:

Amazon S3 (storage)

Amazon CloudFront (fast global delivery)

 Step 1: Create a simple website

On your computer:

1. Create a folder my-website

2.0Inside it, create a file index.html

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

1.0Go to AWS Console

2. Search for S3

3. Click Create bucket

4. Give a unique name (e.g., my-aws-site-12345)

5. Choose region (closest: Mumbai)

6. Uncheck "Block all public access"

7. Create bucket

✅ Step 3: Upload Website Files

1. Open your bucket

2. Click Upload

3. Add your index.html

4.Click Upload

✅ Step 4: Enable Static Website Hosting

1. Go to Properties tab

2. Scroll to Static website hosting

3. Enable it

4. Enter:

Index document: index.html

5. Save

👉 You’ll get a Bucket Website URL

✅ Step 5: Make Files Public

1. Go to Permissions tab

2. Add bucket policy:

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
