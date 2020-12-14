---
title: Какво представляват Java Web Apps ?
last_modified_at: 2020-09-18T08:39:08+00:00
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
Днес приложенията са навсякъде около нас. Дали това ще са app-овете, които използваме локално на смартфоните и лаптопите си, или ще са уеб приложенията, който браузваме в интернет, факт е, че ги изпалзваме постоянно в ежедневието си. Ако сте се чудили каква механика работи зад красивия интерфейс на фейсбук например, или как пишейки в Google името на даден сайт, бързо успявате да го достъпите, то сега ще разгледаме как работят уеб приложенията и какво всъщност представляват.

## Какво е Web Application и как работи?

Представете си, че имаме имаме една празна кутия, това ще е кутията за нашия **web application**. В тази кутия ще сложим кода на наешето приложение (напр. Java код), ще сложим още някакви необходими описателни конфигурации и други файлове нужни на нашият app. Нашата кутия ще е сложена на един от &#8220;рафтовете&#8221; на сървър, който се намира в сървърно помещение.<figure class="wp-block-image size-large is-resized">

<img loading="lazy" src="https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3-1024x683.jpg" alt="" class="wp-image-566" width="450" height="300" srcset="https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3-1024x683.jpg 1024w, https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3-300x200.jpg 300w, https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3-768x512.jpg 768w, https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3-1536x1024.jpg 1536w, https://www.dev-guide.org/wp-content/uploads/2020/09/what-are-java-web-apps-1-3.jpg 1920w" sizes="(max-width: 450px) 100vw, 450px" /> <figcaption>Photo by [Science in HD](https://unsplash.com/@scienceinhd?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com/s/photos/server?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)</figcaption></figure> 

  
  
Ако трябва да дадем някакво просто определение за web application, то ще звучи така:

Web apps са такъв тип програми, които могат да се изпълняват на повече от едно устройства, като те се локализират на сървъри, а достъпът до тях се осъществява посредством мрежа (напр. Internet). Достъпът до уеб приложенията се осъществява чрез уеб браузър (напр. Chrome, Mozilla и др). Тоест, когато отворим нашият любим браузър и напишем в търсачката (браузнем), например _www.wikipedia.org_, се изпраща заявка до сървъра на този web app. Заявката всъщност казва, че искаме да отворим или изпълним това приложение. Важно е да споменем, че сървърът, където се намира нашият web app, &#8220;слуша&#8221; за точно определен URL адрес (наречен **base URL**).
