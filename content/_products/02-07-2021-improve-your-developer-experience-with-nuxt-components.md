---
layout: product
title: Improve Your Developer Experience With Nuxt Components
date: 2021-07-02T12:19:32.061Z
thumbnail: /images/uploads/how-i-created-a-software-company-at-the-age-of-24.png
rating: 7
version: v10.32.0
price: 19
description: >-
  

  ## Introduction


  The Nuxt team has introduced **[@nuxt/components](https://www.npmjs.com/package/@nuxt/components)** module with the purpose to make Nuxt development faster and to make you, as a developer, more productive. This module comes with amazing features and options that will improve your development experience with Nuxt. No matter if you’re just starting out or an advanced user, [@nuxt/components](https://github.com/nuxt/components) provides a range of options from the simplest setup to advance configurations that will certainly benefit your projects.


  In a nutshell, this module automatically scans, imports and registers Vue components found in the **`~/components`** directory, so that we don't have to write import statements when we use them in either pages, layouts or even within components.


  Here is how [Debbie O’Brien](https://twitter.com/debs_obrien) explains how it works,


  > *This module parses your template and automatically includes the component in the file where you are using it such as a page, layout or even a component. Because Nuxt.js uses automatic code splitting to split your pages by default this module works perfect as it will only contain the components that are used on that page. Also, if you use a component in more than 2 pages, Nuxt.js will automatically create a shared chunk for them thanks to the magic of WebPack.*


  ## [](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#table-of-contents)Table of Contents


  * [Introduction](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#introduction)

  * [Table of Contents](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#table-of-contents)

  * [Module Setup](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#module-setup)

  * [Cheatsheet](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#cheatsheet)

  * [Directory path as a String](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#directory-path-as-a-string)

  * [Directory path as an Object](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#directory-path-as-an-object)

    * [Try it yourself - Directory Paths](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#try-it-yourself---directory-paths)
template_feature: >-
  

  * [Directory path as an Object](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#directory-path-as-an-object)

    * [Try it yourself - Directory Paths](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#try-it-yourself---directory-paths)
  * [Inclusion paths](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#inclusion-paths)

    * [Extensions option](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#extensions-option)
    * [Try it yourself - Extensions](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#try-it-yourself---extensions)
    * [Pattern option](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#pattern-option)
    * [Default](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#default)
    * [Add additional extensions](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#add-additional-extensions)
    * [Customize as per your requirement](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#customize-as-per-your-requirement)
  * [Exclusion paths](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#exclusion-paths)

    * [Ignore option](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#ignore-option)
    * [.nuxtignore, ignore property & ignore option:](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#nuxtignore-ignore-property--ignore-option)
  * [Lazy loading your components](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#lazy-loading-your-components)

    * [Try it yourself - Lazy-loading](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#try-it-yourself---lazy-loading)
  * [Third-party component library](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#third-party-component-library)

    * [Try it yourself - Third-party library](https://nuxtjs.org/blog/improve-your-developer-experience-with-nuxt-components#try-it-yourself---third-party-library)
gallery:
  - imgTitle: Image Gallery
    imgSrc: /images/uploads/my-success-story.jpg
  - imgTitle: Gallery item 2
    imgSrc: /images/uploads/আমি-যেভাবে-ফুলস্ট্যাক-ওয়েভ-ডেভেলপার-হলাম.jpg
---
