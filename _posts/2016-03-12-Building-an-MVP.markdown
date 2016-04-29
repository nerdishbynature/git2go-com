---
layout: post
title: Building an MVP
twitter_username: pietbrauer
categories: blog
readtime: 6 min read
---

Launching an Minimum Viable Product (MVP) is not an easy task, nor does everyone understand what it means. The term is a synonym for half-backed products and tight deadlines but is in fact a nice tool to narrow down features and focus. We launched Git2Go as an MVP 5 months ago and this is how it came to be what it is today.


It came to my suprise today when I opened Timehop and saw that one year ago I had taken a day off to work on Git2Go to make some progress, which I couldn't have achieved on evenings or weekends during my full-time job. This was something I never had done for any other side project. 

I felt so committed to shipping a version of Git2Go that I took a vacation day, paid a day in the coworking space nearby and got to work. It was still very early days in the application. All that worked was login with GitHub, showing commits and listing branches. We still had plenty of features to implement before we would consider it a ship-able product. Or so we thought.

Later that year another application launched without us noticing it. As soon as we did, we knew we weren't the only ones with brilliant minds and so we sat together in an "emergency meeting" and cut out features we thought we could do later and instead focus on our vision: Make a user friendly productivity app for iOS devices.

We settled on a MVP. Wikipedia describes a Minimum Viable Product as:

*[...] the minimum viable product (MVP) is a product which has just enough features to gather validated learning about the product and its continued development. Gathering insights from an MVP is often less expensive than using a product with more features which increase costs and risk in the case where the product fails, for example due to incorrect assumptions. [...]* [Wikipedia][1]

This seems easy enough but still confuses people. Some may use it as an excuse to sacrifice quality and get out early, others see it as a synonym for a not reachable deadline, but it is neither.
It's focusing to cut down cost and development time to get to market quicker, with the same quality you wanted in your initial product.
I found a tweet in my timeline lately that confuses the term and I would like to take it as a speaking example:

<blockquote class="twitter-tweet" data-lang="de"><p lang="en" dir="ltr">I can&#39;t thank <a href="https://twitter.com/destraynor">@destraynor</a> enough for making this image. Use it on a monthly basis to avoid cutting quality corners. <a href="https://t.co/n9gPy6t965">pic.twitter.com/n9gPy6t965</a></p>&mdash; Kyle Murphy (@noluckmurphy) <a href="https://twitter.com/noluckmurphy/status/700695023428325376">19. Februar 2016</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

The tweet shows a burnt pizza with the headline "The Minimum Viable Pizza" and the following description:

* Hypothesis: Can we sell pizza for profit?
* Time to produce the pizza: 4 minutes
* Cost: 1 out of 5 Dollar signs
* Learning: No demand for pizza.

There are several things that are horribly wrong in this picture:

## This is not a Minimum Viable Pizza

The fact that this is not a minimum viable pizza is disturbing enough. A minimum viable pizza would be a Pizza Margherita. It is essentially a Pizza but to proof your hypothesis you would still make the best Pizza on the planet to make a demand for your product. Your Pizza would focus on the few ingredients that go into a Pizza: Wheat, Water, Yeast, Olive Oil, Salt, Mozzarella and Tomato. The same is true when building an app or a website. You make sure the few features you pack into it are the best you can come up with. 

This shows early users that you are a good chef/maker and that you care about your users and products. The lack of ingredients or features becomes a second or third thought in your users mind. They will say: "This Pizza is awesome, I can't wait until you put some Mushroom and Olives on it." Instead of: "This Pizza clearly lacks some ingredients and I will not eat it."

## It takes more than 4 minutes to burn a pizza

Even if your oven has two hundred degrees celsius your pizza would clearly take more than fifteen minutes to be burnt to that degree. It would also highlight your lack of focus because it takes some time until a Pizza in an oven goes from well done to "now the whole house smells like burnt wood". 
Your lack of attention as a maker or product manager during these crucial minutes will make the Pizza burn. 
The same is true for your product. It takes time for your product to go from "well done" to "We added over 200 features" and it is your responsibility alone to define when you release it or take it out of the oven. 

Not focusing on your feature set will make a product smell burnt and this will turn away early users. The same applies not only to the outside but also to the inside, your code base, it is simply over done and needs improvement.

## It is not a cheap Pizza

The Pizza above may look cheap but your electricity or gas bill will be higher than it would have been for baking it just right. Your team spent more time and resources on a burnt product than concentrating on a good MVP in the first place. It took longer to make, all ingredients are now waste and because no one wants it, your team morale and reputation are at its lowest. You will probably not do another pizza/product together because it didn't work out. This is clearly not the concepts fault but your managing and execution.

## You haven't learned anything

If after your miserable Pizza cooking your conclusion is "No demand for Pizza" than the fact that you are a bad product owner/maker manifests in your users mind.
The only learning you have after launching should be "No demand for burnt Pizza". Your company vision will probably pivot, too. From making Pizza to making Pasta.
Instead of hiring Pasta chefs and selling your oven, you should step back and look at your core product. What went wrong in your initial launch? The steps should be simple: cut down on features and improve your execution and quality.

## MVP in Git2Go

Fortunate enough we already know Pizzas are delicious and a lot of people want to have one each day. This was not the case with Git2Go, we did not know if it would work on an iPhone or iPad or if anyone wanted to use it as badly as we did. In our emergency meeting we settled down on the launch feature set:

- Login with GitHub
- Clone a repository
- Display the history
- Create and checkout local and remote branches
- List and edit files
- Make Commits
- Push & Pull from one remote

All the features in the initial launch were features we needed to make ourself happy so we could use it whenever we needed to. As our app was born out of necessity to blog on the iPad or iPhone, we only needed to Clone, Edit, Commit and Push. If the launch would fail we would still have a product we could use ourselves. 

The same you can apply to the Pizza: If at the end of the day no one wants to eat your Pizza you would still have a meal for yourself.

[1]:	https://en.m.wikipedia.org/wiki/Minimum_viable_product