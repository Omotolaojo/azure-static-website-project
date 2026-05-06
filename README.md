# azure-static-website-project

# 🚀 Production-Ready Static Website Hosting on Azure

## 🌐 Live Demo
👉 https://www.foojo.name.ng

---

## 📌 Project Summary
This project simulates a real-world deployment for a startup (**Your Techie Hub**) that requires a fast, secure, and globally accessible landing page **without managing servers**.

The solution is designed using Azure-native services to deliver:
- Low latency worldwide
- Secure HTTPS access
- Scalable, serverless infrastructure
- Cost-efficient hosting

---

## 🧠 Architecture Overview


### 🔍 How It Works

| Component              | Role |
|----------------------|------|
| Azure Front Door     | Global entry point, routing, and HTTPS termination |
| Azure CDN            | Caches content at edge locations for fast delivery |
| Azure Storage        | Hosts static website files |
| DNS (CNAME)          | Maps custom domain to Front Door endpoint |

---

## ⚖️ Key Design Decisions

### Why Azure Front Door instead of just CDN?
- Provides **global routing + failover**, not just caching  
- Handles **SSL termination at the edge**  
- Enables future scalability (multi-region backends)

👉 CDN alone improves speed, but **Front Door adds resilience and control**

---

### Why Static Website Hosting?
- Zero server management  
- Lower cost compared to App Services or VMs  
- Ideal for landing pages and frontend apps  

---

## 🏗️ Implementation Steps

### 1. Storage Setup
- Created Azure Storage Account  
- Enabled static website hosting  
- Uploaded site files (`index.html`, CSS, JS)

---

### 2. Front Door Configuration
- Created Front Door profile  
- Added Storage endpoint as backend  
- Configured routing rules for traffic distribution  

---

### 3. CDN Integration
- Enabled caching for static assets  
- Reduced latency via edge delivery  

---

### 4. Custom Domain Mapping
- Connected domain: `foojo.name.ng`  
- Configured DNS (CNAME → Front Door endpoint)

---

### 5. HTTPS Enablement
- Enabled Azure-managed SSL certificate  
- Enforced HTTPS redirection  

---

## 🔐 Security Considerations

- HTTPS enforced across all endpoints  
- Azure-managed certificates with auto-renewal  
- Storage account configured for restricted access  

---

## ⚡ Performance Strategy

- Edge caching via CDN  
- Global routing with Front Door  
- Static hosting eliminates backend processing delays  

---

## 💰 Cost Consideration

This architecture is optimized for **low-cost operation**:

| Service            | Cost Efficiency |
|-------------------|----------------|
| Storage Account    | Pay-per-use (very low for static files) |
| Front Door         | Scales with traffic |
| CDN                | Reduces origin load (cost-saving at scale) |

👉 Compared to VM/App Service hosting, this reduces cost significantly for static workloads.

---

## 🧩 Challenges & Resolutions

| Challenge | Resolution |
|----------|-----------|
| DNS propagation delay | Waited and verified using DNS tools |
| HTTPS certificate delay | Allowed time for validation and rechecked domain mapping |
| Backend routing issues | Corrected origin configuration in Front Door |

---

## 📸 Evidence (Screenshots)

> (To be added — critical for credibility)

- Storage static website enabled  
- Front Door routing configuration  
- Custom domain resolution  
- HTTPS secure connection (browser padlock)

---

## 📊 Future Improvements

- CI/CD pipeline using GitHub Actions  
- Monitoring and alerting with Azure Monitor  
- Web Application Firewall (WAF) integration  
- Multi-region failover setup  

---

## 📚 Key Learnings

- Designing cost-efficient cloud architectures  
- Understanding edge networking (CDN + Front Door)  
- DNS and domain integration in production environments  
- Deploying secure, scalable serverless applications  

---

## 📁 Project Structure
- /website
- ├── index.html
- ├── styles.css
- └── assets/
- README.md


---

## 👤 Author

**Favour Omotola**  
Aspiring DevOps Engineer | Cloud & Infrastructure Enthusiast  

---

## 🚀 Next Step
This project is part of my journey into DevOps and Cloud Engineering.  
I am actively building real-world projects focused on:
- Cloud infrastructure
- Automation
- Scalable deployments
