# 📊 Analyzing HTTP Logs using Splunk SIEM  

## 📌 Overview  
This project focuses on **analyzing HTTP logs using Splunk SIEM (Security Information and Event Management)** to monitor, detect, and investigate potential security threats. By leveraging **Splunk’s powerful log analysis capabilities**, this project helps in extracting **valuable insights** from HTTP logs, identifying suspicious activities, and improving overall cybersecurity posture.  

## 🛠 Technologies & Tools Used  
- **Splunk SIEM** – Log collection, monitoring, and analysis  
- **Kali Linux** – Hosting and simulating attack scenarios  
- **HTTP Logs** – Primary data source for analysis  
- **Regex & SPL (Splunk Processing Language)** – Querying and filtering logs  

## 🎯 Objectives  
✔ **Ingest HTTP logs into Splunk** for real-time monitoring  
✔ **Analyze user activities** to detect anomalies and potential attacks  
✔ **Identify security threats** such as SQL injection, brute force attacks, and unauthorized access attempts  
✔ **Generate reports and dashboards** for better visualization and threat intelligence  

## 🔍 Data Sources  
- **Web server logs** from Apache/Nginx  
- **Firewall and IDS/IPS logs**  
- **Authentication logs**  
- **Custom logs from simulated attacks**  

## 🚀 Implementation Steps  
1. **Set up Splunk SIEM** on the system  
2. **Configure data inputs** to ingest HTTP logs  
3. **Use Splunk SPL queries** to extract insights  
4. **Detect security anomalies** such as repeated failed logins or suspicious IP addresses  
5. **Create visual dashboards and alerts** for real-time monitoring  

## 📊 Example SPL Queries  
- **Finding all failed login attempts**  
  ```spl
  index=web_logs "login failed" | stats count by src_ip
  ```
- **Detecting SQL injection attempts**  
  ```spl
  index=web_logs uri_query="*union select*" OR uri_query="*' OR 1=1--*" | table _time, src_ip, uri_query
  ```
- **Identifying high-volume requests from a single IP**  
  ```spl
  index=web_logs | stats count by src_ip | sort - count
  ```

## 📸 Dashboard & Visualization  
*(Include screenshots of Splunk dashboards and reports for better understanding if available.)*  

## 🔄 Installation & Usage  
1. Clone the repository:  
   ```bash
   git clone https://github.com/ramansinghtanwar/Future_CS_03.git
   cd Future_CS_03
   ```
2. Install Splunk and configure HTTP log ingestion.  
3. Import sample log data for analysis.  
4. Use provided **SPL queries** to generate reports and security insights.  

## 🛡️ Security Insights & Benefits  
✅ **Real-time monitoring** of HTTP logs for security threats  
✅ **Early detection** of brute-force, SQL injection, and DDoS attacks  
✅ **Customizable dashboards** for a clear security overview  
✅ **Actionable threat intelligence** for cybersecurity teams  

## 📄 Project Link  
🔗 [Analyzing HTTP Logs using Splunk SIEM](https://github.com/ramansinghtanwar/Future_CS_03/blob/main/Project-analyzing-http-logs-using-splunk-siem.md)  

---

 😊
