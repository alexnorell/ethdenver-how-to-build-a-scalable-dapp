---
title: "Hugo-Webslides"
---

Hugo-Webslides
Use markdown to write contents and render with WebSlides to HTML. { .text-intro }

{{< svg fa-github >}}Github

WebSlides Demos
Here's what you can do with WebSlides.

{{< gallery title="Why WebSlides" href="#slide=10" src="https://webslides.tv/static/images/demos-why.png" >}}Why WebSlides{{< /gallery >}}
{{< gallery title="Landings" href="https://webslides.tv/demos/landings" src="https://webslides.tv/static/images/demos-landings.png" >}}Landings{{< /gallery >}}
{{< gallery title="Portfolios" href="https://webslides.tv/demos/portfolios" src="https://webslides.tv/static/images/demos-portfolios.png" >}}Portfolios{{< /gallery >}}
{{< gallery title="Keynote" href="https://webslides.tv/demos/apple" src="https://webslides.tv/static/images/demos-apple.png" >}}Keynote{{< /gallery >}} { .flexblock .gallery }
More Examples
Note. None of these slides are currently ported to Hugo-Webslides...YET.

{{< gallery title="Netflix's Culture" href="https://webslides.tv/demos/netflix-culture" src="https://webslides.tv/static/images/demos-netflix.png" >}}Netflix{{< /gallery >}}
{{< gallery title="Longform Articles" href="https://webslides.tv/demos/longforms" src="https://webslides.tv/static/images/demos-longforms.png" >}}Longforms{{< /gallery >}}
{{< gallery title="Interviews" href="https://webslides.tv/demos/interviews" src="https://webslides.tv/static/images/demos-interviews.png" >}}Interviews{{< /gallery >}} { .flexblock .gallery }
Configuration
You can modify WebSlides settings directly from your project config.toml. { .text-intro }

[params.webslides]
  banner = false
  slideshow = true
  vertical = false
  autoslide = false
  changeOnClick = false
  disableLoop = false
  minWheelDelta = 40
  disableNavigateOnScroll = false
  scrollWait = 450
  slideOffset = 50
  hideIndex = false
|||v

All from one markdown file
Use three dashes "-" to create a separate slide page.

|||

Slide1

---

Slide2
|||

content
├── home
│   ├── home1.md (weight: 1)
│   └── home2.md (weight: 2)
└── _index.md (initial page)
|||

Or not.
You can combine and arrange files with the weight parameter in front matter, and categorize .md files into different folders.

Slide Attributes
Assign attributes to a slide by using the following notation.

---
<!-- : .class .class2 ..sub-class bg=bg-class bgimage=(frame|dark|light)|http://image-url/ bgpos=POSITION -->
<section id="section-x" class="bg-class slide current" style="">
  <span class="background-POSITION" style="background-image:url('http://image-url/')"></span>
  <span class="background frame"></span>
  <div class="class class2">
    <div class="sub-class">
      CONTENT
    </div>
  </div>
</section>
Assign class to elements
note: depreciated with the introduction of Hugo's native block attribute

{{< flexblock "Headers and Paragraphs" 6 >}} # <!-- : .hClass -->Header
<!-- : .pClass -->Paragraph
<h1 class="hClass">Header</h1>
<p class="pClass">Paragraph</p>
{{< /flexblock >}}

{{< flexblock "Lists" 6 >}} <!-- : .listClass -->
- list1
- list2
<ul class="listClass">
  <li>list1</li>
  <li>list2</li>
</ul>
{{< /flexblock >}} { .flexblock }