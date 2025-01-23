# WordPress Media Offloading with Amazon Lightsail

This project demonstrates how to configure a WordPress website to offload media to Amazon Lightsail's object storage and deliver content via a Lightsail distribution. By following this guide, you can improve media delivery performance, SEO, and reduce server load.

## Features
- 📦 Automatic media upload to Amazon Lightsail buckets.
- ⚙️ Easy integration with WordPress using the WP Offload Media Lite plugin.

---

## Prerequisites
Before you begin, make sure you have:
1. An Amazon Lightsail account.
2. A WordPress website (hosted on Lightsail or elsewhere).
3. Basic knowledge of WordPress and AWS services.

---

## Setup Instructions

### Step 1: Create a Lightsail Bucket
1. Log in to the Amazon Lightsail console.
2. Create a bucket to store your media files.
3. Enable public access for the bucket (required for serving content).
![create-a-bucket](https://github.com/user-attachments/assets/79c6cb42-1892-4ecb-acda-0c2523a53826)

### Step 2: Install WP Offload Media Lite Plugin
1. Log in to your WordPress dashboard.
2. Navigate to **Plugins > Add New**.
3. Search for **WP Offload Media Lite** and click **Install Now**.
4. After installation, click **Activate**.

### Step 3: Configure the WP Offload Media Lite Plugin
1. Go to **Settings > Offload Media** in your WordPress dashboard.
2. Select **Amazon S3** as the storage provider.
3. Choose **My server is on Amazon Web Services, and I'd like to use IAM Roles**.
4. Select your Lightsail bucket.
5. Enable:
   - **Force HTTPS**: Ensures media is served securely.
   - **Remove Files From Server**: Reduces disk usage on your server.
6. Configure delivery:
   - Choose **Amazon CloudFront**.
   - Add your distribution’s default domain (e.g., `123abc.cloudfront.net`) or custom domain (e.g., `media.mycustomdomain.com`).

### Step 4: Test the Setup
1. Upload a media file via the WordPress **Media Library**.
2. Check the file’s URL—it should point to your distribution.
3. Verify the file exists in your Lightsail bucket under the `wp-content` folder.

![verify yfile exists in your Lightsail bucket](https://github.com/user-attachments/assets/800b5ca8-fd0a-4720-a816-577d4233a955)

![verify-file-exists-in-your-Lightsail-bucket](https://github.com/user-attachments/assets/c4a28dd6-bb85-4e6a-87af-62573004755e)

## Benefits
- **Cost Efficiency**: Reduces storage and bandwidth usage on your WordPress server.
- **Scalability**: Seamlessly handle increased traffic and media requests.

---

## Troubleshooting
- **Media Not Offloading**: Verify the WP Offload Media Lite plugin settings.
- **Bucket Missing Files**: Ensure the plugin is active and correctly configured.

---

## License
This project is licensed under the [MIT License](LICENSE).

---

## Resources
- [AWS Hands-on-tutorial: Connecting a WordPress website to an Amazon Lightsail bucket and distribution
with Amazon Lightsail](https://aws.amazon.com/getting-started/hands-on/object-storage-cdn/)
- [Amazon Lightsail Documentation](https://docs.aws.amazon.com/lightsail/)
- [WP Offload Media Lite Plugin](https://deliciousbrains.com/wp-offload-media-lite/)
- [WordPress Documentation](https://wordpress.org/support/)

