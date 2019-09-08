# WebSite publishing demo

Demo of publishing a static website on GitHub.

## Steps 

### 1. Create repository

The first step is to create the repository for the website you wish to publish.

### 2. Push your code

The HTML file with name `index.html` will be published as the home page. If there is no `index.html` file, then it searches for `README.md` file and that markdown file will be published as the homepage.

### 3. Publish GitHub Page

Click on the settings tab, scroll down to `GitHub Pages` section and select `master branch`.

### 4. Go to website

You can go to the published website after 15–20 seconds

This site is published at [https://fvarrui.github.io/website-demo/](https://fvarrui.github.io/website-demo/).

### 5. Adding CNAME to GitHub repo

First of all, you’ll need to add a CNAME file to your GitHub repo. Now, just as adding a normal file.

Create a new file called `CNAME` (without any extension) and in that file, add the domain name (eg. `fvarrui.es`) then commit and push the changes.

### 6. Adding A Records with your DNS provider

This step (adding A record) will be done on the side of your DNS provider.

In this step we will be creating an `ALIAS` or `ANAME` record, or simply, `A` record that points to the IP (or domain) of GitHub Pages server.

Doing this is very simple, all you need to do is find a section on the website of your domain name provider where you can add A records. Generally this section itself is called DNS. Once you find it, add the following IP addresses in the `Points To` field.

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

For complete documentation on setting up an apex domain, [click here!](https://help.github.com/articles/setting-up-an-apex-domain/#configuring-a-records-with-your-dns-provider).







