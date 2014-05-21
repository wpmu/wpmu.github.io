---
layout: blog
title:  "Re-thinking the Shoestrap Theme"
category: development
permalink: blog/rethinking-shoestrap
tags: development, twig
---

When we set out to create the Shoestrap theme 2 years ago, we wanted to build a theme that would allow anyone to build a great, unique site without being a developer.
A theme that would be simple enough to operate by anyone, but would still appeal to developers because of its great extensibility.

We recently came to the realization that the Shoestrap theme is not what we started out to do.
Instead of being a light, fast theme that can be easily customized, it has become slow, bulky and full of options that -though useful to some- simply make the interface more cluttered and difficult.

A few months ago we re-coded many parts of the theme, focusing on improving and fine-tuning the admin interface as well as fix bugs that were present for a long time and have been neglected.
As it turns out, **we were wrong**.
Though the theme is now more stable than ever, we feel like we are still a long way from what we originally set out to do.

With this in mind, we decided to completely re-build the theme.

Those of you that have been using Shoestrap since the beginning might remember that up until version 2.0 (now in the [legacy branch](https://github.com/shoestrap/shoestrap-3/tree/legacy) of our gihub repository) we were using the WordPress Customizer and had no admin panel.
We then jumped to version 3.0 that included Bootstrap 3.0 and instead of using the Customizer switched to the amazing [Redux Framework](http://reduxframework.com/).
As a matter of fact, [@dovy](https://twitter.com/SimpleRain), one of our lead developers for Shoestrap 3.0 experimented with all other frameworks available and decided Redux was worth investing on. He is now a fulltime developer on developer there (as seen on the [redux repository statistics](https://github.com/ReduxFramework/redux-framework/graphs/contributors)) and we couldn't have been more grateful for what he has done.

**Redux is a beast**. It's a massive, amazing beast. One we don't use to its full extent because quite simply we don't need to.
So we took a step back and started re-thinking everything.

## What do we **really** want shoestrap to be?
Well, we want it to be a free, open-source theme that will do its job right.
We see hundreds of themes on a daily basis. Some free, others premium.
Most of them are use-case-specific. Some focus on bloging, others on portfolios, business directories and pretty much all you can think of.
The ones that don't focus on a specific use-case are -like Shoestrap- cluttered and heavy.

We want Shoestrap to be easy to use and even easier to customize.
So the next version will be **completely** different:

* We started writing the theme from scratch
* We will not use redux. Instead we'll switch back to the WordPress Customizer.
* We will use [twig](http://twig.sensiolabs.org/) for our templates

### Why start from scratch?

Starting from a clean codebase without taking anything for granted will allow us to build a theme like it's supposed to be.

As much as we like the Roots theme and we've been using it for the past 2 years as the base of our theme, we feel like it is no longer necessary for us to use it. Though it has some great elements, it is not where we want to head. By starting from scratch we'll be able to build everything cleaner and leaner, document everything better and also as a bonus we'll be able to remove all functionality that usually belongs in a plugin and not a theme. These options will be included in a separate plugin.

### Why we won't be using redux

As mentioned above, we use only parts of the redux framework. By removing it we will be able to use the WordPress Customizer. This will allow our users to have a faster site and also be able to preview their changes in real time.
We've already added a lot of custom controls to the customizer and tweaked its look. The result of our Customizer modifications can also be used by other themes and is available as a separate plugin called [Kirki](http://kirki.org).

### Why use twig?

Twig is a templating language that will allow non-developers to write their own templates. It's a lot easier to understand than PHP (which is not really a templating language) and will allow our users to become more involved.

To this end, we have included [Timber](http://jarednova.github.io/timber/) in the theme.

An additional benefit of this is that we'll also be able to write implementations for other CSS frameworks easier and more effectively using [twig macros](http://twig.sensiolabs.org/doc/templates.html#macros).

## Compatibility

Since we started building this theme from scratch, we are not building this with the sole purpose of building an "updated" version of Shoestrap. No... Coding-wise, this will be a completely different theme. We will however write (after we've completed its development) a migration script that will allow our users to update from version 3 to this new and improved theme.

The update process will be smooth and until we finish writing this new version, no new features will be implemented on the current version, only bugfixes.

We would like to call you to contribute your opinions or even your own code to our new github repository on [https://github.com/wpmu/shoestrap](https://github.com/wpmu/shoestrap).

Feel free to download or fork this and play with it!


