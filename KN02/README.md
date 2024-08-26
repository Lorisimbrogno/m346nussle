#Lab 4.1 EC2
##AWS MODULE 1 Notizen

##Aufgabe 1

### Impact of Cloud Computing on Society

Cloud computing has significantly democratized access to advanced technologies, enabling even small businesses and individuals to utilize powerful computing resources without large upfront investments. This shift has fostered innovation, collaboration, and global access to data and services.

### Surprising Information

It was surprising to see how much cloud computing has accelerated the growth of startups by allowing rapid scaling and reducing financial barriers to entry.

### Sources and Credibility

Information was sourced from credible industry reports (Gartner, IDC), academic journals, and trusted news outlets like *The New York Times*. These sources are reliable due to their rigorous research, peer review, and expert analysis.

##Aufgabe 2

### Differences in Cloud Service Use

- **IaaS:** infrastructure as a Service. Businesses rent computing resources like servers and storage, ideal for flexibility and control.
- **PaaS:** Platform as a Service. Provides platforms for developing and managing applications, streamlining the development process.
- **SaaS:** Software as a Service. Offers software on a subscription basis, commonly used for tools like CRM and office productivity.

### Most Important Service

**SaaS** is likely the most important, as it provides easy, cost-effective access to essential software, allowing businesses to focus on their core activities.

### Advice for Starting a Business

Start with **SaaS** for essential tools, then consider **IaaS** or **PaaS** as your business grows and needs more flexibility or custom development.
<br>
#AWS MODULE 2

##Den Rest einfach gelesen.

#AWS MODULE 4.1
HTML Seite:
http://54.162.58.76/
![alt text](image.png)
Running Instances:
![alt text](image-1.png)
Details der Webserver Instanz:
![alt text](image-2.png)
Inbound Regel:
![alt text](image-3.png)

#Lab 4.2 S3
Liste der Buckets:
![alt text](image-4.png)
HTML Seite:
http://modulm346loris.s3-website-us-east-1.amazonaws.com/
![alt text](image-5.png)
Liste der Dateien im Bucket:
![alt text](image-6.png)
Eigenschaften von "Static Website Hosting"
![alt text](image-7.png)
Json für öffentlichen Zugriff:
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::modulm346loris/*"
        }
    ]
}

