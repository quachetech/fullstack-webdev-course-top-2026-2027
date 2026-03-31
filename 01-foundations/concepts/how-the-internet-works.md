# How The Internet Works

**Date Learned:** 31 March 2026  
**Related Lesson:** [How Does The Web Work](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)  
**YouTube Explanation:** [Day 3: How The Internet Works](https://youtu.be/m0UeSgzwFBg)

---

## 🎯 What Is This?

The internet isn't magic—it's infrastructure, protocols, and clever systems working together.

---

## 🧠 Why Does It Matter?

Understanding this helps you:

- Debug faster (if a website is down, is it a domain issue? Server issue? Network issue?)
- Choose hosting wisely (shared hosting vs dedicated servers vs cloud)
- Optimize performance (latency matters—CDNs, caching, server location)
- Build better apps (knowing how requests travel helps you write efficient code)

---

## 🛠️ How It Works

### 🔐 Three Levels of Network Access
The same internet infrastructure can be configured for different levels of privacy:
**1. Intranet (Private)**

A company's internal network
Only employees' devices can access it
Example: Your company's internal file server, employee portal

**2. Extranet (Semi-Private)**

Opens part of the intranet to trusted external partners
Example: A supplier accessing your company's ordering system, or clients accessing a project dashboard

**3. Internet (Public)**

Open to anyone in the world
Example: Google, YouTube, any public website

**Key insight:** It's not three TYPES of internet—it's three ACCESS LEVELS using the same underlying tech.

### 🛰️ Internet Infrastructure (How Data Travels)
Data moves through different physical mediums:
1. Fiber Optic Cables → Fastest, lowest latency (light pulses through glass)
2. Copper Wires → Slower than fiber, older tech (electrical signals)
3. Satellites → Higher latency (signal travels to space and back), but works in remote areas
4. Cell Towers → Wireless, medium speed, powers mobile internet
Latency = delay between request and response. Lower latency = faster internet.
***Why this matters for developers:** When you build apps, you optimize for latency. Users on satellite internet have a worse experience than fiber users—your code needs to account for this.

### 🏷️ IP Addresses vs Domain Names
Every device connected to the internet gets an IP address (a unique number like 172.217.164.46).
Problem: Humans can't remember 172.217.164.46. We remember google.com.
Solution: Domain names are human-readable aliases that POINT to IP addresses.
How it works:

You type google.com in your browser
DNS (Domain Name System) looks up the IP address for google.com
Your browser connects to that IP address
The server at that IP sends you the Google homepage

**Key point:** Domain names are assigned to IP addresses, and IP addresses are assigned to SERVERS (computers), not websites.

### 💾 Servers: The Computers That Host Websites
What's a server?
A server is just a computer that's always on, connected directly to the internet, storing files (websites, databases, etc.) on its SSD (solid-state drive).
**Two scenarios:**
***Scenario 1: Dedicated Server***

Google has entire data centers (thousands of servers) dedicated ONLY to Google services
google.com points to Google's server IP address
That server ONLY serves Google's website

***Scenario 2: Shared Hosting***

Small websites (like a local bakery or personal blog) share ONE server with 10, 100, or 1000 other websites
Problem: All those websites can't use the SAME IP address (would cause conflicts)
Solution: Host headers (the server checks which domain name you requested—bakery.com vs blog.com—and serves the right website)

**Key insight:** IP addresses belong to SERVERS, not websites. When multiple websites share a server, the server uses host headers to figure out which website to serve.


### Example:


---

## 🔗 Key Terms

- **Internet** Infrastructure that enables computer dvevices to connect, communicate and share information with each ither.

---

## 📌 Common Misconceptions

- The web and the internet are the same: one is a service (web) while the other is infrastructure (internet). The web is a service the that is built upon the infrastructure that is the internet.

---

## 🚀 Next Steps

How the web works

---

**Feynman Test:** Can I explain this to someone with zero coding knowledge?  
✅ Yes