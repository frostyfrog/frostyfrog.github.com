---
layout: post
title: What is HTML?
categories: [html, webdev]
author: colton
---
Welcome to the first in a series of tutorials for learning how to make web sites. Bear with me now, because this ride may get bumpy!

* [The Basics](#the_basics)
* [XML](#xml)
* [HTML](#html)
* [Extra](#extra_tags)

The Basics
==========
Now the first time you see HTML, you'll probably wonder what everything is. But first, let me explain something simpler. HTML is based off of XML, so let's start with that.

XML
---
XML is one of the more basic languages when it comes to web pages. Let's take a look, shall we?

	<root>
		<item1>
			<subItem var="1">
				<subSubItem />
			</subItem>
			<subItem></subItem>
			<subItem />
		</item1>
		<item2>Hello World!</item2>
	</root>

I'm not sure about you, but that's pretty simple. Not simple? Let me explain. XML has different "tags". Now these tags can be named anything, but the must contain an *opening* (`<item1>`) tag and a *closing* (`</item1>`) tag. Sometimes, they can be opened and closed with only one tag (``<subItem />``), but there is a limitation with that. No content.

In fact, the only tag that we do have content in, is `<item2>Hello World!</item2>`.

If you noticed the tag `<subItem var="1">`, you may have wondered what I did there. Tags can also have extra data stored in them that is not content. In this case, we are assigning `var` to the number `1`.

Now, that just about covers XML. I hope that was a good enough explanation. Now, on to the structure of HTML.

*Edit: I was talking to [Lothus Marque][LM] and they stated the following.*
> **(19:13:17) Lothus Marque: I would have said XML was based on HTML, just with a far more rigorous structure requirement.   It came later, after all.**

> (19:14:50) frostyfrog: Ah, well. That's new to me.   I'm self taught, so I assumed HTML was based off of XML since XML seems way more lax on what tags you use. As I said in there though, I prefer XHTML 1.0 Strict doctype.

> (19:15:29) frostyfrog: Seems to work nearly everywhere.

> **(19:15:58) Lothus Marque: They've got different intents. HTML was, and is, a generalized markup language. XML has far more strict requirements on tagging, and is better suited for structured data. XHTML, though they're still dealing with XHTML5 as part of HTML5, is not really the way most people recommend that I've seen any more. XHTML showed up in the "XML IS GOD AND EVERYTHING" phase. :/**

[LM]: http://www.mercenary-enclave.com/ (The website of Lothus Marque)
HTML
----

Now that we have XML out of the way, it is time to move on to HTML. First thing that we need to specify, is the DOCTYPE (Short for *Document Type*) tag. The DOCTYPE tag informs the browser how to handle the web page.
If we didn't tell the browser how to handle the web page, it would look different in between browsers. There wouldn't be a fluid experience for the user, except for those who are using the exact same web browser (Internet Explorer, Google Chrome, Firefox, Opera, etc.) that you are using.
There are [Multiple Different Doctype Declarations](http://www.w3.org/QA/2002/04/valid-dtd-list.html) available, but for the most part, I prefer to stick with XHTML 1.0 Strict. In later tutorials, I might switch to the new (HTML5) spec.

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
	   "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

Although there are other Doctypes available, I choose this one because it seems the most cross-browser compatible. Now, on with the basic structure.

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
	   "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
	<html>
		<head>
			<title>My Webpage Title</title>
		</head>
		<body>
			<h1>It works!</h1>
			<p>I have successfully made my first web page, and it looks like it works! Yay! =D</p>
		</body>
	</html>

Does the structure and the concept of tags look familiar? Well, it is. We are just adding limits and context to them now. That may look like a lot, but the only thing that the user will see is in the `<body>` tag. Let me break that all down.

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
	   "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">

This is the Doctype for XHTML 1.0 Strict.

	<html>

`<html>` tells the browser that everything inside is the HTML web page.

	<head>
		<title>My Webpage Title</title>
	</head>

`<head>` is called head because it's at the start of the web page. It's also where you will put styles, dynamic scripts, and other fun tags (Like `<title>`)

The `<title>` tag is a little hidden, but if you look at the tab name (Or your browser's title), you will find it there.

Finally, we close the `<head>` tag.

		<body>
			<h1>It works!</h1>
			<p>I have successfully made my first web page, and it looks like it works! Yay! =D</p>
		</body>

Here is the `<body>` tag that we mentioned earlier. Let's see what's inside.

Here we have the `<h1>` tag. Then inside it, we have the text "It works!" After which, we close the `<h1>` tag. H1 is the biggest header element you will have. All of the header tags are, in order: h1, h2, h3, h4, h5, h6.

In the case of this page, here is how all 6 work. Try tinkering around with the number in the code to see what you get.
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6

Next up, we have the `<p>` tag. This just signifies that there is a paragraph of text. Though it's not needed, it does help the code look a bit prettier.

And now we have the `</body>` closing tag (Sound familiar?) signifying that we are done with the body of the web page.

	</html>

Now we are at our final piece of code. I don't think I need to explain this again, but I will anyways. With the `</html>` closing tag, we are now signifying that we are done with our entire web site.

Extra tags
----------
Now I'm going to quickly mention a few tags for you to play around with and see what you can do.

`<b></b>` and `<strong></strong>` add **emphasise** to what you are saying.

`<i></i>` and `<em></em>` makes your viewers *turn their heads in confusion*.

`<u></u>` is used for <u>underlining</u> things like titles, headers, etc.

That's all for this blog entry.

<!-- http://jekyllbootstrap.com/lessons/jekyll-introduction.html -->
