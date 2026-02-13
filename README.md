🚀 LearnFlow

A full-stack video sharing and discussion platform built with Node.js, Express, MongoDB, EJS, AWS S3, and CloudFront.
Users can authenticate via Google, upload videos with thumbnails, and engage in deeply nested comment discussions.

📸 Application Preview

1️⃣ Landing Page

Clean and modern entry interface.

<img width="100%" src="https://github.com/user-attachments/assets/f442949b-f637-4acd-a74a-f28eb6ec3cc2" />

2️⃣ Google Authentication

Secure login using Google OAuth.

<img width="100%" src="https://github.com/user-attachments/assets/dc032ba9-8def-4ad5-9ef2-e2499f397ec7" />

3️⃣ Dashboard

Centralized hub for user activity and content.

<img width="100%" src="https://github.com/user-attachments/assets/f73784ca-6531-44a6-afaa-a5c9ca465904" />

4️⃣ Create Post

Upload video + thumbnail with rich description.

<img width="100%" src="https://github.com/user-attachments/assets/0b171209-9e75-4ef0-8731-f042d4ba0782" />

5️⃣ Post Created

Successful upload with CDN-backed media delivery.

<img width="100%" src="https://github.com/user-attachments/assets/8b679ebb-0238-46a8-bf4f-cf8be05671bf" />

6️⃣ View Posts

Watch videos delivered via CloudFront CDN.

<img width="100%" src="https://github.com/user-attachments/assets/00bf5493-2aad-4800-bb36-2abf165ae3c9" />

7️⃣ Infinitely Nested Comments

Threaded discussions with recursive rendering.

<img width="100%" src="https://github.com/user-attachments/assets/f4061539-2a3e-4171-bb5a-b7f44f2569c9" />

🔐 AWS Configuration
S3

Private bucket

CORS enabled

Object upload via presigned URL

Block Public Access enabled

CloudFront

Origin Access Control (OAC)

HTTPS only

Cached content delivery

Restricted S3 access

☁️ CloudFront Configuration

CloudFront is configured as a secure CDN layer in front of a private S3 bucket to deliver uploaded videos and thumbnails globally with low latency.

Origin: Amazon S3 (your_bucket_name)

Origin Access: Origin Access Control (OAC) enabled

Bucket Visibility: Private (Block Public Access ON)

Viewer Protocol Policy: Redirect HTTP → HTTPS

Allowed Methods: GET, HEAD

Cache Policy: Managed-CachingOptimized

WAF: Disabled (AWS Shield Standard enabled by default)

Access Control: S3 bucket policy restricts access to this CloudFront distribution only

🔁 Media Flow

Upload: Frontend → Presigned URL → S3

Delivery: User → CloudFront → Private S3

⚙️ Environment Variables

Create a .env file:

PORT=3000

MONGO_URI=your_mongodb_connection

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_secret

AWS_REGION=select_region
AWS_ACCESS_KEY_ID=your_iam_access_key
AWS_SECRET_ACCESS_KEY=your_iam_secret
S3_BUCKET=your_bucket_name
CLOUDFRONT_URL=your_cloudefront_url

▶️ Installation
https://github.com/warhead12/Learn_flow.git
cd learnflow-pw-25-main
npm install
npm start

📦 Folder Structure (Simplified)
routes/
models/
views/
public/
middleware/
config/

📈 Future Improvements

Video streaming optimization (HLS)

Like / Subscribe system

Pagination & lazy loading

WebSocket-based real-time comments


👨‍💻 Author
Abhishek Anand
Built with focus on scalability, clean architecture, and cloud-native best practices.




