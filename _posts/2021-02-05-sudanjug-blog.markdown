---
layout: post
title:  "How to write a post on SudanJUG Blog - كيف تكتب موضوع علي مدونة موقع مستخدمي جافا"
date:   2021-02-05 22:30:23 +0200
categories: blog sudanjug
author: Ghazy Abdallah
published: true
---

### How to write a post on SudanJUG's blog

Did you know [sudanjug.github.io](https://sudanjug.github.io) website is completly open source? and that anyone can post on the blog section? all you need is just a little bit knowledge in Git and Github, if you don't you can use this [guide](https://guides.github.com/activities/forking/) along the steps.

The website is build using [Jekyll](https://jekyllrb.com) a static sites generator written in Ruby, but you don't have to know Ruby to publish a blog post, here's how you can do that in just a few minutes:

1. Write your post in [Markdown](https://www.markdownguide.org/) format, if you need help with that you can use free online tools like [StackEdit](https://stackedit.io).
2. [Fork](https://guides.github.com/activities/forking/) website's [Git repository here](https://github.com/SudanJUG/sudanjug.github.io).
3. Create a markdown file inside ```_posts``` directory.
4. Name the file in the following pattern ```YYY-MM-DD-your-blog-title.markdown``` example ```2021-02-01-moved-by-java.markdown```.
5. Place this snippet at the top of the file, then place your post Markdown text below it.
```
---
layout: post
title:  "your-blog-title"
date:   2021-02-05 22:30:23 +0200
categories: blog sudanjug your-category
author: your-name
published: true
---
your-post-content-here
```
6. [Save](https://guides.github.com/activities/forking/#making-changes) your file in Git.
7. Do a [pull request](https://guides.github.com/activities/forking/#making-a-pull-request)
8. A maintainer will review and accept your pull request.
9. Your post is now live 🎉 see it [here]({% link blog.html %}).

---

### كيف تكتب موضوع علي مدونة موقع مستخدمي جافا

هل تعلم ان [هذا الموقع](https://sudanjug.github.io) مفتوح المصدر بشكل كامل؟ وانه يمكن لاي شخص  نشر مواضيع علي المدونة؟ كل ماتحتاجة هو القليل من المعرفة ب قيت و قيت هب، اذا كنت لاتملك المعرفة فيمكنك الاستعانة بهذا [الدليل](https://guides.github.com/activities/forking/).

الموقع مصمم بتقنية [جيكل](https://jekyllrb.com) مولد صفحات ساكنة بلغة برمجة روبي، ولكن لاتقلق لاتحتاج معلرفة بلفة روبي لتتمكن من نشر موضوع، اليك كيفية فعل ذلك في دقائق قليلة:

1. اكتب الموضوع بتنسيق [مارك داون](https://www.markdownguide.org/), اذا كنت لاتعرف فيمكنك استخدام خدمات مجانية لمساعدتك مثل [ستاك ايدت](https://stackedit.io).
2. قم [بنسخ](https://guides.github.com/activities/forking/) الموقع من [مستودع قيت هب](https://github.com/SudanJUG/sudanjug.github.io).
3. قم بانشاء ملف جديد علي المسار ```_posts```.
4. قم بتسمية الملف بالصيغة
```YYYY-MM-DD-your-blog-title.markdown```
5. قم باضافة النص ادناة اعلي الملف, ومن بعدة نص الموضوع
```
---
layout: post
title:  "your-blog-title"
date:   2021-02-05 22:30:23 +0200
categories: blog sudanjug your-category
author: your-name
published: true
---
your-post-content-here
```
6. قم [بحفظ](https://guides.github.com/activities/forking/#making-changes) الملف علي المستودع.
7. قم بانشاء [طلب دمج](https://guides.github.com/activities/forking/#making-a-pull-request)
8. سنقوم بمراجعة الطلب والموافقة عليه.
9. تهانينا 🎉 اطلع عليها [هنا]({% link blog.html %}).

#SudanJUG #MovedbyJava