# AWS Static Website Hosting (S3 + CloudFront + GitHub Actions)

This project hosts a static website on **Amazon S3** and delivers it globally using **Amazon CloudFront (HTTPS)**.  
Deployment is automated using **GitHub Actions CI/CD**, and CloudFront cache is invalidated after every update.

---

## ✅ Live Links
- **GitHub Pages (Free Demo):** https://yaraganidurgadhanush.github.io/my-aws-static-website/
- **CloudFront (HTTPS):** https://d3kelxivb1qmsg.cloudfront.net
- **S3 Website Endpoint:** http://sree-static-website-01.s3-website-us-east-1.amazonaws.com

---

## 🛠 Technologies Used
- HTML
- CSS
- AWS S3 (Static Website Hosting)
- AWS CloudFront (CDN + HTTPS)
- AWS IAM (Access keys for deployment)
- GitHub Actions (CI/CD)

---

## 🚀 Features
- Static website hosted on S3
- Secure delivery using CloudFront (HTTPS)
- Auto deployment to S3 on every push to `main`
- Automatic CloudFront cache invalidation for instant updates

---

## ⚙️ CI/CD Workflow
GitHub Actions runs on every push to `main` and deploys the website using:

----

## 🗺️ Architecture Diagram

![AWS CI/CD Architecture](assets/aws_cicd_architecture.png)


```bash
aws s3 sync . s3://sree-static-website-01 --delete
