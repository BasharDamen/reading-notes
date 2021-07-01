# Error Handling & Debugging   


# How to Debug JavaScript Errors #  

Debugging JavaScript errors in a production environment can be a difficult experience. More often than not, the error reports are vague, and identifying the underlying causes can be difficult at best. That said, there are a few common steps that can be followed towards identifying and resolving errors that crop up in production.  

![error](https://cdn.searchenginejournal.com/wp-content/uploads/2021/01/common-seo-ranking-603e51c401a8d.png)

---

## Gathering information ##  

### **Step 1: Attempt to replicate circumstances** ###  

In software development, the first step towards debugging any issue is attempting to replicate the circumstances. With most programming languages, this is bolstered by reviewing logs leading up to an error, but with client-side JavaScript, this type of diagnosis requires significantly more foresight.  

Before we can replicate any circumstances of an issue, and assuming we have access to any production logs, we first need to establish some testing guidelines. This involves doing things like mimicking the production database, the user accounts involved, and even the operating system. Everything is fair game here.  

### **Step 2: Test assumptions** ###  

Once you've established the circumstances that you think might throw the exception or error you are hunting down, it's time to test them. `Never test exceptions in production.` Development and staging environments are designed to be breakable without any impact on the end users, so always always always try to break your code in a safe environment.  

### **Step 3: Increase logging** ###   

More information is always better. The first step towards diagnosing any issue is to increase the amount of data you are logging. This allows you to see everything that is happening before and after a problem occurs. There is a good chance that the problems you are experiencing have potential warnings associated with them that don't necessarily make it into the logs by default.  

### **Step 4: Adjust test parameters and try again** ### 

If you were unable to replicate the problem in Step 2, then it's back to the drawing board. Not every error is easy to reproduce, and may have time-based constraints or something else making it difficult to replicate in a non-production environment. Jump back to Step 1, adjust your test parameters, and try it all over again.  

---

## What are Source Maps? ##  

In a production environment, JavaScript files are often compressed. While this is a great way to speed up any application, it can make debugging a nightmare, as the files you are trying to debug are practically unreadable. This is where source maps come into the picture. Supported by most modern browsers, a source map is a file that maps uncompressed code to compressed code, allowing you to see exactly what is going on within a production environment.  

In a production environment, JavaScript files are often compressed. While this is a great way to speed up any application, it can make debugging a nightmare, as the files you are trying to debug are practically unreadable. This is where source maps come into the picture. Supported by most modern browsers, a source map is a file that maps uncompressed code to compressed code, allowing you to see exactly what is going on within a production environment.  

While most minification tools have built-in support for source maps, it is important to understand exactly how the browser connects compressed code to uncompressed code. In a nutshell, this comes in the form of a comment within a compressed JavaScript file that points directly to the source map.

> `//# sourceMappingURL=http://example.com/path/to/your/sourcemap.map`  


### **Stack Traces in JavaScript** ###  

Whenever exceptions are thrown, a stack trace is usually included. But, what is a stack trace? In essence, it is a rundown of every file and function that is called leading up to the error. To be clear, a stack trace doesn't include the files and functions that are touched before the error occurred, only the chain of methods that are called as the error happened. This allows you to "trace" the "stack" of operations that are performed when an error happened in order to identify exactly what went wrong, and where.

![error](https://bugfender.com/wp-content/uploads/2020/09/Featured-scaled.jpg)