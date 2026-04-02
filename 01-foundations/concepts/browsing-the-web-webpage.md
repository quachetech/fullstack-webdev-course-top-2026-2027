# Browsing The Web: Webpages & URLs

**Date Learned:** 02 April 2026  
**Related Lesson:** [How Does The Web Work](https://theodinproject.com/lessons/foundations-how-does-the-web-work)  
**YouTube Explanation:** [...]()

---

## 🎯 What Is This?

So in today's lesson, I covered browsing the web but looking specifically at the webpage. It is a simple HTML document displayed by a browser and can embed a variety of different types of resources like style information which controls it's look and feel, script which adds interactivity to the page, as well as media that is images sounds and videos. 

Browsers can also display other documents such as PDF files and other resources such as images and videos but the term webpage specifically refers to an HTML document. so each webpage is found in a unique location and has web address called a URL, and to access the page you just type the address in the browser's address bar.

**Uniform Resource Locator (URL)** is a string of text that specifies where resources (such as a video, image or webpage) can be found on the internet. 

---

### 🧠 Key Concept: What is a Webpage?

A webpage is an **HTML document** displayed in a browser.

**It can embed:**
- Style information (CSS) → controls look and feel
- Scripts (JavaScript) → adds interactivity
- Media → images, sounds, videos

**Key distinction:** "Webpage" specifically means HTML documents (not PDFs, images, or videos—even though browsers can display those too).

---

### 🔗 URLs: The Address System of the Web

**URL = Uniform Resource Locator**  
A string of text that specifies WHERE a resource (webpage, image, video) is located on the internet.

**My Insight:** URLs look like file paths on my computer—and they work the same way!

---

### 🧩 Breaking Down a URL

**Example:**
```
https://theodinproject.com/lessons/foundations-how-does-the-web-work
```

**Structure:**

| Part | What It Is | Purpose |
|------|-----------|---------|
| `https://` | **Protocol** | Tells the browser HOW to access the resource (securely) |
| `theodinproject.com` | **Domain Name** | Alias for the server's IP address (which server to contact) |
| `/lessons/foundations-how-does-the-web-work` | **Path** | Where the file is stored on the server (like a directory path) |

---

### 💡 The Connection: URLs = File Paths

**On my local computer:**
```
/home/kuda/Documents/coding/project.html
```

**On a web server:**
```
https://theodinproject.com/lessons/foundations-how-does-the-web-work
```

**Both are hierarchical addresses pointing to a specific file.**

**The difference:**
- Local paths start from my computer's root directory (`/home`)
- URLs start with a protocol and domain (`https://theodinproject.com`)

But the PRINCIPLE is the same: **a systematic way to locate a resource.**

---

### 🔍 How It Works (My Understanding)

When I type a URL in my browser:

1. **Browser reads the protocol** (`https://`) → "Okay, secure web access"
2. **Browser reads the domain** (`theodinproject.com`) → Asks DNS: "What's the IP address?"
3. **DNS responds** → `104.21.34.78` (example IP)
4. **Browser connects to that server**
5. **Browser sends the path** (`/lessons/foundations-how-does-the-web-work`) → "Give me this file"
6. **Server finds the file** in its directory structure
7. **Server sends the HTML file back**
8. **Browser displays the webpage**

---

### 🎯 Why This Matters

Understanding URLs helps me:
- Debug broken links (is the path wrong? domain wrong? protocol wrong?)
- Organize files when I build my own website
- Understand how browsers find resources

**URLs are the addressing system of the web—just like IP addresses, domain names, and file paths.**

**Everything connects.** 🧩

---

## 🚀 Next Steps

Browsing the Web: Websites

---

**Feynman Test:** Can I explain this to someone with zero coding knowledge?  
✅ Yes