# AWS 

## cloudfront
1. Save data in S3, make it public 
2. Services -> cloudfront -> Distributions

### Create Distribution -> get start

#### Origin Settings
- Origin Domain Name <- 
- Origin Path <- 
- Origin ID <- 
- Origin Custom HeadersHeader NameValue <- 
 
#### Default Cache Behavior Settings
Path Pattern Default (*)		

Viewer Protocol Policy
- HTTP and HTTPS
- Redirect HTTP to HTTPS
- HTTPS Only <- 

Allowed HTTP Methods
- GET, HEAD <- 
- GET, HEAD, OPTIONS
- GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE
Field-level Encryption Config

Cached HTTP Methods  
- GET, HEAD (Cached by default) <- 

Cache and origin request settings
- Use a cache policy and origin request policy <- 
- Use legacy cache settings

Cache Policy
- Managed-CachingOptimized or Create a new policy <- 
- View policy details

Origin Request Policy
- Create a new policy or View policy details <- 

Smooth Streaming
- Yes
- No <- 

Restrict Viewer Access
(Use Signed URLs or Signed Cookies)
- Yes  <- 
- No

Compress Objects Automatically
- Yes <- 
- No

Lambda Function Associations <- default
- CloudFront Event
ViewerRequest
ViewerResponse
Origin Request
Origin Resonse
- Lambda Function ARN	
- Include Body

Enable Real-time Logs
- Yes
- No

Distribution Settings
- Price Class
- Use All Edge Locations (Best Performance)
- AWS WAF Web ACL

Alternate Domain Names (CNAMEs)

SSL Certificate
- Default CloudFront Certificate (*.cloudfront.net)
- Custom SSL Certificate (example.com): <- 
You can use a certificate stored in AWS Certificate Manager (ACM) in the US East
(N. Virginia) Region, or you can use a certificate stored in IAM. 
Request or Import a Certificate with ACMLearn more about using custom SSL/TLS certificates with CloudFront.
Learn more about using ACM.

Supported HTTP Versions
- HTTP/2, HTTP/1.1, HTTP/1.0
- HTTP/1.1, HTTP/1.0

Default Root Object <-

Standard Logging
- On
- Off <-

S3 Bucket for Logs <-
Log Prefix <-

Cookie Logging
- On
- Off
Enable IPv6 <- yes

Distribution State
- Enabled
- Disabled


## NAT Gateway
EIPなしで、外部のネットワークにアクセスには、NAT Gatewayを通る必要がある
### 手順
aws -> vpc -> NAT Gateways -> create NAT Gateway

VPC -> Route Talbes

0.0.0.0/0 nat-0019f023efe84762a


## cognito


## docs.xxxxdata.com
1. S3
2. CloudFont
3. ACM (better in same region)
4. Configure DNS
