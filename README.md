

## 🌐 Project : Multi-Tier VPC Isolation & Connectivity

**Objective:** To design and validate a secure network architecture that protects sensitive backend data from public internet exposure.

### **🛠️ Infrastructure Overview**

I manually architected a custom Virtual Private Cloud (VPC) to simulate a real-world enterprise environment:

* **Public Subnet (Frontend):** Configured with an **Internet Gateway** and a specific **Route Table** entry (`0.0.0.0/0`) to allow web traffic.
* **Private Subnet (Backend):** Logically isolated by removing all internet routes, ensuring that resources like databases remain unreachable from the outside world.

### **✅ Security Validation (The Proof)**

I verified the security of this architecture through two distinct tests:

1. **Public Connectivity Test:** Verified that the frontend instance can successfully reach the internet for updates.
* **Evidence:** `vpc-public-ping-success.png`


2. **Private Isolation Audit:** Verified that the backend instance is 100% isolated.
* **AWS Console Check:** Confirmed "Instance is not in public subnet" warning.
* **Connectivity Check:** Confirmed a "Network is unreachable" failure during a ping test.
* **Evidence:** `vpc-private-isolation-proof.png` and `vpc-private-ping-fail.png`



### **📈 Skills Demonstrated**

* **Network Design:** Custom VPC creation and CIDR block management.
* **Traffic Control:** Configuring Internet Gateways, Route Tables, and Subnet Associations.
* **Security Posture:** Implementing the "Principle of Isolation" to protect high-value cloud assets.

---

### **A Pro-Tip for your GitHub**

Since you are a **First Year BCA student**, adding a "Troubleshooting" note about the **CIDR overlap error** you encountered will show recruiters that you have real hands-on experience and problem-solving skills.

**Would you like me to help you write a 1-sentence "LinkedIn Headline" that highlights both your IAM and VPC projects?**
