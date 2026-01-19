# AWS Static Website Hosting (S3 + CloudFront + GitHub Actions)

This project hosts a static website on **Amazon S3** and delivers it globally using **Amazon CloudFront (HTTPS)**.
Deployment is automated using **GitHub Actions CI/CD**.

---

## ✅ Live Links
- **CloudFront (HTTPS):** https://d2eve86rl9u63o.cloudfront.net
- **S3 Website Endpoint:** http://sree-static-website-01.s3-website-us-east-1.amazonaws.com

---

## 🛠 Technologies Used
- HTML
- CSS
- AWS S3 (Static Website Hosting)
- AWS CloudFront (CDN + HTTPS)
- IAM (Access keys for deployment)
- GitHub Actions (CI/CD)

---

## 🚀 Features
- Static website hosted on S3
- Secure delivery using CloudFront (HTTPS)
- Auto deployment to S3 on every push to `main`

---

## ⚙️ CI/CD Workflow
GitHub Actions runs on every push to `main` and deploys the website using:

```bash
aws s3 sync . s3://sree-static-website-01 --delete
