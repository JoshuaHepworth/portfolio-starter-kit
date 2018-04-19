# Portfolio Starter Kit

## Objectives

- Build a cool portfolio
- Get hosting and a custom domain name
- Host our cool portfolio on our custom Domain Name

## Repo

First thing's first - create a new repo for your project. FROM SCATCH - don't fork this repo. Initialize it with a readme and an index.html file that gives a simple 'hello world':

```html
	<!DOCTYPE html>
	<html>
	<head>
		<title>My Portfolio</title>
	</head>
	<body>
		<h1>Hello World!</h1>
	</body>
	</html>
```

Once you set up hosting, you'll be able to drop this into your root directoy as a simple test to see if you've established a connection. A very useful tool!

> There's a sample index.html file in this repo, but once again, **do not build your project on this repo**.

## Hosting

Let's start with the more technical side of this project - getting hosting and a domain name. 

Purchasing hosting is, in a nutshell, the equivalent of renting a folder on a server for your project to live in. Much like renting an apartment, quality and cost can varry wildly. Here's a few suggestions for reliable hosting companies:

-[Github](https://help.github.com/articles/using-a-custom-domain-with-github-pages/) - You already know it, and it's free! You'll have to jump through some hoops to set up it, though - documentation can be found [here](https://help.github.com/articles/using-a-custom-domain-with-github-pages/).
- [Dreamhost](https://www.dreamhost.com/) - Standard fair hosting service. around $25/mo. Handles domain, email, and other common services for you. Almost unlimited storage. See also: [Bluehost](https://www.bluehost.com/).
- [Amazon Web Services](https://aws.amazon.com/) - Cheap and scalable - only pay for what you use (could be as low as $1-3/mo). No frills. 
- [Heroku](https://heroku.com/) Cloud app hosting - Probably overkill for what you need, but good if you want to scale to hosting full apps. Price tiers based on usage, from free to $500/mo.

- Never use GoDaddy. _Never use GoDaddy_.

Each hosting service will have its own way of handling how your files are stored and updated. You'll need to read their documentation to understand how that works.

## Domain Names (DNS)

Domain names are NOT technically part of your hosting package. Once your website has its metaphorical appartment, it can only be reached by an IP number. For instance, to get to Google without using it's Domain Name, you can go to 8.8.8.8.

Many services like Dreamhost will sell you a domain name as part of your hosting package. **This is your best option, as its often difficult to coordinate the ownership of your DNS.** If the hosting you pick doesn't offer this, make sure you buy your domain from a reputable company, like [Google](https://domains.google/#/). There is a [very real blackmarket for Domain Names](https://gimletmedia.com/episode/7-this-website-is-for-sale/) that you will want to avoid.

### Top Level Domains

![URL anatomy](http://eloquence.co.nz/wp-content/uploads/2013/07/URL-anatomy.jpg)

Your website can end with a lot more than .com - here's a complete rundown:

- .com - standard, totally fine

- .co - cool and new, common amongst web devs

- .___ (new top level domains): http://data.iana.org/TLD/tlds-alpha-by-domain.txt - great if relevant

- .net, .biz - NEVER.

## Site Architecture

While we've learned a lot of fancy tools to make full-stack sites, you probably won't need any of that in order to make a great portfolio site. My suggestion for your portfolio is to make a simple, static, purely frontend site using HTML, CSS, minimal JS, and probably Bootstrap. Your entire site architecture might look something like this:

- root
	- index.html 
	- css
		- bootstrap.css
		- main.css
	- js
		- main.js

> Many personal portfolio sites are only a single page. This is a common design trend you'll see on Bootstrap template sites.


### Bootstrap Templates

Bootstrap templates

Using a template for your personal site is generally a bad idea - but since you've had only minimal design training, and will have very little time to devote attention to your webitse pre-grad, this is probably going to be neccessary. Given the choice between a poorly-designed site you made yourself, and a great site you used a template for, employers would rather see the later. The work INSIDE your portfolio will speak to your skill as a developer.

Here's some good places to find Bootstrap templates:

- [Start Bootstrap](https://startbootstrap.com/)
- [Shape Bootstrap](https://shapebootstrap.net/free-templates)
- [Wrap Bootstrap(not free)](https://wrapbootstrap.com/?ref=bsw)

> Make sure that you test the template you pick on multiple screen sizes and browsers. Dig in and learn what they're leveraging with Bootstrap, and how. This can help you replicate the same functionality when you create your own from sites scratch.

## Deploying your Site

Your hosting company should provide you with a list of ways to deploy your site to the live hosting environment. A common method is FTP, in which you upload your files through an FTP client like [FileZilla](https://filezilla-project.org/) or [CyberDuck](https://cyberduck.io/). The obvious downside of this is that there is no built-in version control - this is why you'll want to work on a github repo regardless of how static your site is, then dump your files on the FTP server after you commit/push.

Another option is some kind of middleware that deploys from your repo for you. [DeployBot](https://deploybot.com/), for example, hooks into both your Github and Hosting account, and pushes from Githubt to your host when you tell it to. 

## Mail Servers

Most hosting services also offer mail through your DNS - i.e., Nick@NickAnderson.Rocks. Using those mail services are up to you. While *in theory* they should be easy to configure and set up, even a small error can cause days of headaches and lost mail. Be sure to read your documentation to determine how easy it will be to set up, how you'll be able to access your mail, and if it costs extra. There is an entire week's worth of classes we could teach on configuring mail servers, so be prepared to read a lot of documentation and Google a lot questions if you go this route. 

![Make sure you understand mail servers before you use them](img/emails.jpg)
*Protip - make sure you understand mail servers before you use them*

It's perfectly normal to have a generic gmail address not associated with your website as your main point of contact. That being said, the effect of a personalized email address on your DNS conveys an even more polished and professional presentation. 

>My suggestion would be to try to set up an email server through your DNS, but don't get it printed on business cards until you are absolutely sure it is functional and usable. 

## Good examples:

- [Nick Anderson](http://nickanderson.rocks/)
- [Matt Webb](http://www.mattwebb.co/)
- [Clay Smith (WDI2)](http://clay-code.com/)
- [Jacy Anderson (WDI3)](http://jacyanderson.co/)
- [Taylor Laine (WDI3)](http://www.taylorlaine.codes/)
- [Cam Barclay (WDI3)](http://camcreates.co/)


## Common Issues and Testing

There's a few things to keep in mind as you progress through this proccess:

1. It will take a while for your hosting/DNS to propagate - sometimes up to 48 hours. Do not be alarmed if you cannot reach your website (either through your browser or FTP) for a couple days after purchasing it.

2. Furthermore, changes made to your hosting environment will sometimes take a few minutes to take affect. Be sure to check caching settings in your hosting service - if your site is being cached, you will not see changes until you hard-refresh or delete your cookies.

3. Don't delete anything in your hosting directory just cause you don't know what it is. Read your hosting documentation and see what it says about any mysterious files or directories you encounter.

4. Don't change settings you don't understand in your hosting account. These will vary by hosting type, but in general, **if you don't know what it is, don't change it.**

## Questions?

Feel free to submit issues to this repo if you have any unanswered questions - just also slack me to notify me of them as well.




