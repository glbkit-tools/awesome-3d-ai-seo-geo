# Awesome 3D AI, SEO & GEO for 3D Web

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re/)
[![3D Web](https://img.shields.io/badge/3D-Web-black.svg)](https://glbkit.com/)
[![AI](https://img.shields.io/badge/AI-3D-blue.svg)](https://glbkit.com/)
[![SEO](https://img.shields.io/badge/SEO-3D%20Web-green.svg)](https://glbkit.com/)
[![GEO](https://img.shields.io/badge/GEO-AI%20Search-purple.svg)](https://glbkit.com/)

> A curated collection of AI, SEO, GEO, AEO, AI search, performance, and developer resources for 3D websites, WebGL applications, Three.js projects, React Three Fiber applications, and modern 3D web experiences.

Building a 3D website is only part of the challenge.

A modern 3D website also needs to be **discoverable, understandable, crawlable, performant, accessible, and useful to both people and search systems**.

This repository brings together practical resources for developers building the modern 3D Web — from 3D development and asset optimization to technical SEO, AI search, Generative Engine Optimization (GEO), Answer Engine Optimization (AEO), and AI Overviews.

The goal is simple:

**Help developers build 3D websites that look great, work well, and can be understood by humans, search engines, crawlers, and AI systems.**

Why this matters more for 3D websites than for typical websites: a 3D site often renders its most important content — a product, a model, a configurator — inside a `<canvas>` element that search engines and AI crawlers cannot directly read. Text baked into a WebGL scene, labels drawn with shaders, or product details that only appear after a user interacts with a 3D viewer are effectively invisible to most of the systems that decide whether your site gets discovered. This repository exists to close that gap: to give 3D developers a single reference for making sure the *engineering* of a great 3D experience is matched by the *discoverability* of that experience.

---

## Table of Contents

* [AI Tools for 3D](#ai-tools-for-3d)
* [AI APIs & Models](#ai-apis--models)
* [AI Search & Answer Engines](#ai-search--answer-engines)
* [AI Overviews](#ai-overviews)
* [GEO for 3D Websites](#geo-for-3d-websites)
* [AEO for 3D Websites](#aeo-for-3d-websites)
* [SEO for 3D Websites](#seo-for-3d-websites)
* [Technical SEO](#technical-seo)
* [Structured Data & Schema](#structured-data--schema)
* [3D Model SEO](#3d-model-seo)
* [WebGL SEO](#webgl-seo)
* [Three.js SEO](#threejs-seo)
* [React Three Fiber SEO](#react-three-fiber-seo)
* [Image & 3D Asset Optimization](#image--3d-asset-optimization)
* [Web Performance](#web-performance)
* [Crawlers & AI Bots](#crawlers--ai-bots)
* [robots.txt](#robotstxt)
* [sitemap.xml](#sitemapxml)
* [llms.txt](#llmstxt)
* [Metadata & Open Graph](#metadata--open-graph)
* [Analytics](#analytics)
* [Search Console Tools](#search-console-tools)
* [Developer Tools](#developer-tools)
* [Learning Resources](#learning-resources)
* [3D Web Resources](#3d-web-resources)
* [3D E-commerce SEO](#3d-e-commerce-seo)
* [3D Tool Website SEO](#3d-tool-website-seo)
* [Recommended 3D Web Architecture](#recommended-3d-web-architecture)
* [How to Use This Repository](#how-to-use-this-repository)
* [Common Mistakes](#common-mistakes)
* [Contributing](#contributing)
* [Support](#support)
* [Related GLBKit Resources](#related-glbkit-resources)
* [License](#license)

---

# AI Tools for 3D

AI is becoming part of many stages of the 3D workflow, from asset creation and texturing to development, documentation, optimization, and content generation.

Across the pipeline — modeling, texturing, rigging, coding, QA, and documentation — AI tools are shifting from novelty to everyday utility. The sections below break this down by workflow stage so you can find the right category of tool for the problem you actually have, rather than the one that's trending.

### AI for 3D Modeling

Useful categories include:

* Text-to-3D generation — turning a written prompt into a base mesh or full asset
* Image-to-3D generation — reconstructing geometry and texture from one or more reference photos
* AI-assisted modeling — in-tool suggestions, auto-completion of geometry, or guided sculpting
* 3D asset generation — end-to-end pipelines that output ready-to-use GLB/glTF files
* Texture generation — AI-generated diffuse, normal, and roughness maps
* Material generation — PBR material creation from text or reference images
* Asset cleanup — automatic mesh repair, hole filling, and non-manifold geometry fixes
* Retopology assistance — reducing dense scan meshes into clean, animation-ready topology
* Animation generation — AI-assisted skeletal animation and motion synthesis
* 3D asset classification — automatically tagging and categorizing large model libraries

When evaluating any AI modeling tool, check the license terms for generated output carefully — some services restrict commercial use of AI-generated meshes or textures, which matters if you plan to sell or redistribute the resulting assets.

### AI for 3D Development

AI coding tools can assist with:

* Three.js
* React Three Fiber
* WebGL
* WebGPU
* GLSL
* TypeScript
* Next.js
* Tailwind CSS
* 3D asset pipelines
* Shader development
* Performance optimization

When using AI-generated code, always review:

* Rendering lifecycle
* GPU usage
* Resource disposal
* Memory usage
* Asset loading
* Browser compatibility
* Accessibility
* Performance

AI-generated Three.js and R3F code is prone to a specific set of recurring mistakes worth watching for explicitly: forgetting to dispose of geometries, materials, and textures when a component unmounts (a common source of GPU memory leaks in single-page apps); creating new objects (vectors, materials, geometries) inside the render loop instead of memoizing them outside it; recommending deprecated APIs from older Three.js versions that no longer match the current release; and missing `useFrame` cleanup in React Three Fiber components. Treat AI output as a first draft that still needs a profiling pass in Chrome DevTools or the Three.js/R3F devtools before it ships.

---

# AI APIs & Models

AI APIs can add intelligent features to 3D applications.

Common use cases include:

* Natural-language product configuration
* 3D asset search
* Model tagging
* Scene descriptions
* Automated metadata
* Product classification
* Image understanding
* Product recommendations
* Natural-language navigation
* Documentation generation
* Asset organization

Useful categories include:

* Large language models
* Vision models
* Multimodal models
* Embedding models
* Image generation models
* 3D generation models
* Speech and voice APIs
* Vector databases
* AI agent frameworks

A practical pattern for 3D tool sites: use a vision or multimodal model to auto-generate an alt-text description and a short product-style summary the moment a user uploads a GLB or GLTF file. That generated text can then populate the page's meta description, an `ImageObject` or `Product` schema entry, and the visible HTML around the viewer — solving three SEO/AEO problems (metadata, structured data, and crawlable content) from a single AI call.

---

# AI Search & Answer Engines

Search is evolving beyond traditional keyword-based results.

Modern websites may be discovered and interpreted through:

* Search engines
* AI-powered search
* Answer engines
* Conversational search
* Retrieval systems
* AI assistants
* Knowledge systems

Developers should understand concepts such as:

* Crawlability
* Retrieval
* Entity understanding
* Content authority
* Structured information
* Source attribution
* Citations
* Topical relevance
* Search intent

For 3D websites, this is especially important because much of the visual experience may exist inside JavaScript and WebGL.

A useful mental model: traditional search engines rank *pages*, while many AI search and answer systems retrieve and synthesize *passages* — a paragraph, a definition, a table row, a single FAQ answer. That means a 3D tool page benefits from having self-contained, clearly-labeled chunks of text (a definition of what the tool does, a short answer to "what formats does this support", a one-paragraph explanation of a feature) rather than one long undifferentiated block of marketing copy.

---

# AI Overviews

AI-generated search summaries can change how users discover websites.

For 3D websites, important information should not exist only inside a WebGL canvas.

For example, a 3D product page should expose useful information through normal HTML:

* Product name
* Product description
* Specifications
* Materials
* Dimensions
* Features
* Compatibility
* Pricing where applicable
* Images
* Related products
* FAQs

The interactive 3D experience should enhance the page rather than become the only source of information.

### Useful Practices

* Write descriptive page titles.
* Use meaningful headings.
* Keep important information in HTML.
* Use structured data where appropriate.
* Build strong internal links.
* Make important entities explicit.
* Provide useful supporting content.
* Keep pages technically crawlable.
* Make important facts easy to understand.

Being cited or summarized inside an AI Overview or an AI chat answer typically depends on the same underlying signals as ranking well organically: clear, factual, well-structured content that directly answers a likely question. There is no separate "AI Overview SEO" trick — the more reliably a page answers "what is this", "how does it work", and "what are the specs" in plain HTML text, the more likely it is to be pulled into a synthesized answer.

---

# GEO for 3D Websites

**Generative Engine Optimization (GEO)** generally refers to improving content so generative search systems and AI assistants can discover, understand, retrieve, and potentially reference it.

For 3D websites, useful GEO practices include:

* Clear entity descriptions
* Strong topical structure
* Helpful supporting content
* Structured data
* Consistent terminology
* Descriptive headings
* Internal linking
* Authoritative references
* Useful product information
* Machine-readable metadata

### GEO Checklist

* Is the main topic immediately clear?
* Can the page be understood without the 3D canvas?
* Are important entities explicitly named?
* Are important facts easy to extract?
* Are related pages internally linked?
* Is the content supported by structured information?
* Does the page provide unique value?

### Practical GEO Techniques for 3D Tool Pages

* Name the tool and its core action in the first sentence of the page (e.g. "GLB Viewer lets you view GLB and glTF files online" rather than a vague tagline).
* Repeat key entity names consistently — don't alternate between "GLB viewer," "3D viewer," and "model viewer" for the same tool across a page; pick one primary term and use it consistently while allowing natural variation elsewhere.
* Answer "what," "how," and "why" for the tool in separate, clearly headed sections rather than one merged paragraph.
* Link each tool page to related tool pages and to any guide or documentation page that expands on it, so a generative system can traverse the site's topical cluster rather than seeing isolated pages.

---

# AEO for 3D Websites

**Answer Engine Optimization (AEO)** focuses on making content useful for systems that answer questions directly.

Useful content formats include:

* FAQs
* Definitions
* Comparisons
* Tutorials
* Specifications
* Troubleshooting guides
* How-to documentation
* Product information
* Technical explanations

A 3D product page, for example, can answer:

* What is this product?
* What materials does it use?
* What formats are supported?
* What are its dimensions?
* How does the 3D viewer work?
* What platforms are supported?

The 3D experience provides the interactive layer while HTML provides the explanatory layer.

FAQ sections are one of the highest-leverage AEO investments for a 3D tool site because they map almost one-to-one onto the kinds of short, specific questions answer engines are built to resolve — "what file formats does this GLB viewer support," "is this tool free," "does this work on mobile." Keep each FAQ answer self-contained (a reader — human or machine — should be able to understand the answer without reading the rest of the page) and avoid answers that simply link elsewhere without giving any direct information.

---

# SEO for 3D Websites

Traditional SEO remains an important foundation for 3D websites.

Core areas include:

* Search intent
* Keyword research
* Page structure
* Semantic HTML
* Internal linking
* Metadata
* Structured data
* Content quality
* Image optimization
* Technical SEO
* Performance
* Mobile usability

### The 3D SEO Principle

> **Use WebGL for interaction and visualization. Use HTML for information.**

Do not make search engines understand information that could simply be provided as accessible HTML.

### Keyword Research for 3D Tools

3D tool keywords tend to fall into a few recurring intent patterns worth researching separately:

* Tool-intent keywords ("glb viewer online", "convert glb to gltf")
* Format/technical keywords ("what is a glb file", "gltf vs glb")
* Comparison keywords ("blender vs three.js for web", "best 3d viewer for websites")
* Integration keywords ("embed 3d model in website", "three.js product viewer")

Each pattern typically deserves its own page or content cluster rather than being squeezed onto a single homepage.

---

# Technical SEO

Technical SEO is particularly important for JavaScript-heavy 3D applications.

Important areas include:

* Crawlability
* Indexability
* Rendering
* Canonical URLs
* HTTP status codes
* Redirects
* Internal links
* Robots directives
* XML sitemaps
* Metadata
* Structured data
* JavaScript rendering
* Performance
* Mobile experience

### JavaScript Applications

For frameworks such as Next.js:

* Server-render important content where appropriate.
* Keep interactive components client-side where necessary.
* Avoid unnecessary client rendering.
* Use meaningful URLs.
* Generate metadata correctly.
* Keep initial HTML useful.
* Load heavy 3D components strategically.

### Rendering Strategies

* **Server-Side Rendering (SSR)** — good for pages where content changes per request and needs to be fresh for crawlers immediately.
* **Static Site Generation (SSG)** — ideal for tool landing pages, guides, and documentation that don't change often; fastest and most crawler-friendly.
* **Incremental Static Regeneration (ISR)** — a middle ground for content that updates periodically (e.g. a model gallery) without a full rebuild.
* **Client-Side Rendering (CSR)** — acceptable for the interactive 3D viewer itself, since the surrounding page shell should already carry the crawlable content.

A common pattern for a Next.js-based 3D tool site: render the page shell, headings, description, and structured data on the server, then dynamically import the `<Canvas>`/Three.js viewer component on the client with a loading fallback, so crawlers get a fully-formed HTML page even before any WebGL code executes.

---

# Structured Data & Schema

Structured data provides machine-readable information about a page.

Potential schema types for 3D websites include:

* `WebSite`
* `WebApplication`
* `SoftwareApplication`
* `Organization`
* `Product`
* `Offer`
* `BreadcrumbList`
* `FAQPage`
* `HowTo`
* `Article`
* `ImageObject`
* `VideoObject`
* `Person`

Only use structured data that accurately describes the page and its visible content.

Useful resources:

* Schema.org
* Google Search Central
* JSON-LD
* Rich Results testing tools

### Notes on Choosing a Schema Type

* A free browser-based tool (like a GLB viewer or screenshot generator) is usually best represented as `WebApplication` or `SoftwareApplication`, not `Product`, since no physical or purchasable good is involved.
* `FAQPage` should only be used on pages that visibly display the same questions and answers as plain HTML — don't mark up FAQ schema for content hidden behind a click with no visible text.
* `HowTo` schema fits step-by-step tool guides ("how to take a GLB screenshot") but should mirror the actual visible steps on the page.
* JSON-LD is generally preferred over microdata or RDFa for modern JavaScript-rendered sites since it can be injected as a single script block independent of the DOM structure.

---

# 3D Model SEO

3D assets can benefit from descriptive metadata and supporting content.

A dedicated 3D model page may expose:

* Model name
* Model description
* Creator
* Category
* File format
* File size
* Polygon count
* Texture information
* Material information
* Animation information
* License
* Dimensions
* Preview images
* Related models

### Descriptive File Names

Prefer:

```text
red-sports-car.glb
```

over:

```text
model-final-v8.glb
```

File names should be descriptive without unnecessary keyword repetition.

### Why This Matters Beyond File Names

Descriptive, consistent metadata isn't just cosmetic — it's what allows a 3D tool site to build meaningful internal linking and faceted browsing (by category, format, license, or creator) without manual curation. A model library with clean, structured metadata can auto-generate category pages, related-model sections, and breadcrumb trails, all of which compound the SEO and GEO value of every individual model page.

---

# WebGL SEO

WebGL provides rendering capabilities, but a canvas does not replace semantic web content.

A WebGL application should generally sit alongside normal HTML content.

### Recommended Structure

```text
HTML
│
├── Title
├── Description
├── Headings
├── Text Content
├── Structured Data
├── Internal Links
├── Images
│
└── WebGL
    └── Interactive 3D Experience
```

The WebGL scene should complement the HTML page.

### Accessibility Considerations

A `<canvas>` element is, by default, an opaque black box to screen readers. Where practical, provide an accessible fallback: a text description of the scene, an ARIA label summarizing what the canvas contains, or a static image alternative for users who cannot or choose not to load WebGL content. This overlaps directly with SEO — the same fallback text that helps a screen-reader user also gives crawlers something to read.

---

# Three.js SEO

Three.js is a 3D rendering library, not an SEO framework.

When building websites with Three.js:

* Keep important information outside the canvas.
* Use semantic HTML.
* Provide meaningful metadata.
* Use crawlable URLs.
* Avoid turning the entire website into one canvas.
* Optimize JavaScript loading.
* Optimize 3D assets.
* Provide accessible alternatives where appropriate.

### Three.js Performance Areas

Pay attention to:

* Geometry complexity
* Texture sizes
* Draw calls
* Materials
* Shadows
* Post-processing
* Animation loops
* GPU memory
* JavaScript bundle size

### Common Three.js Pitfalls That Also Hurt SEO/Performance Scores

* Loading the full Three.js bundle plus unused examples/addons instead of tree-shaking imports.
* Instantiating a new `WebGLRenderer` context per component instead of sharing one across a page.
* Failing to call `.dispose()` on geometries, materials, and textures when swapping models, leading to memory growth that eventually degrades Core Web Vitals like Interaction to Next Paint.
* Running the animation loop (`requestAnimationFrame`) even when the canvas is off-screen or the tab is inactive, wasting CPU/GPU and battery.

---

# React Three Fiber SEO

React Three Fiber provides a declarative way to build Three.js experiences with React.

For SEO-sensitive applications:

* Keep SEO content outside `<Canvas>`.
* Server-render important content where appropriate.
* Separate marketing content from interactive 3D components.
* Dynamically load heavy 3D components when useful.
* Keep metadata independent from the WebGL scene.

### Recommended Pattern

```text
Page
│
├── SEO / Marketing Content
├── Product Information
├── Structured Data
│
└── Interactive 3D Viewer
    └── React Three Fiber Canvas
```

### R3F-Specific Notes

* Use `next/dynamic` (or the equivalent in your framework) with `ssr: false` to load the `<Canvas>` component only on the client, while keeping the surrounding page server-rendered.
* Keep `useFrame` callbacks lightweight; heavy per-frame logic inside R3F components is one of the most common sources of dropped frames on lower-end mobile GPUs.
* Where drei or other R3F helper libraries are used, only import the specific helpers needed rather than the entire package, to keep the client JavaScript bundle small.

---

# Image & 3D Asset Optimization

Large assets can significantly affect the performance of 3D websites.

## Images

Consider:

* Responsive images
* Modern image formats
* Correct dimensions
* Lazy loading
* Descriptive alt text
* Compression

## 3D Models

Useful technologies and formats include:

* GLB
* glTF
* Draco
* Meshoptimizer
* KTX2
* Basis Universal
* Texture compression
* Geometry optimization
* Level of Detail

Do not optimize only for download size.

Also consider:

* Decode time
* GPU memory
* CPU usage
* Rendering cost
* Mobile performance

### A Practical Optimization Checklist for GLB/glTF Files

* Compress geometry with Draco or Meshoptimizer before shipping to production.
* Compress textures to KTX2/Basis Universal where the target browsers support it, rather than shipping raw PNG/JPEG textures inside the GLB.
* Generate multiple Levels of Detail (LOD) for complex models so mobile devices can load a lighter mesh.
* Strip unused animations, cameras, and lights that were exported by default from DCC tools like Blender.
* Re-check file size *and* GPU decode/upload time after each optimization pass — a smaller file that still takes a long time to decode on-device hasn't solved the real problem.

---

# Web Performance

3D websites can be visually impressive while still being expensive to load and render.

Important areas include:

* Core Web Vitals
* Largest Contentful Paint
* Interaction to Next Paint
* Cumulative Layout Shift
* JavaScript execution
* Network requests
* Image loading
* 3D asset loading
* GPU performance
* Memory usage

### Practical Strategy

A useful approach is:

```text
Load the page
      ↓
Render useful content
      ↓
Load the interactive experience
      ↓
Load additional 3D assets when needed
```

Avoid making a large 3D scene unnecessarily block the initial experience.

### Core Web Vitals, Specifically for 3D Pages

* **Largest Contentful Paint (LCP):** avoid letting the 3D canvas itself be the LCP element if it loads slowly — make sure meaningful text or a poster image paints first.
* **Interaction to Next Paint (INP):** heavy per-frame WebGL work can block the main thread and delay responses to clicks/taps; move non-rendering work (parsing, decompression) off the main thread with Web Workers where possible.
* **Cumulative Layout Shift (CLS):** reserve a fixed-size container for the canvas before the 3D content loads, so the layout doesn't jump once the viewer initializes.

---

# Crawlers & AI Bots

Websites may be accessed by many different automated systems.

These can include:

* Search engine crawlers
* AI crawlers
* Social media crawlers
* Preview bots
* Security scanners
* Performance tools
* Link crawlers

Important questions include:

* Can the page be crawled?
* Can important HTML be retrieved?
* Are useful resources blocked?
* Is the sitemap available?
* Are canonical URLs correct?
* Are unnecessary routes excluded?
* Does the page return the correct HTTP status?

### Identifying Crawler Traffic

Server logs and analytics tools can help distinguish between different crawler types by user agent (search engine bots, AI training/retrieval crawlers, social preview bots such as those used by messaging apps). Reviewing this traffic periodically helps confirm that important pages are actually being fetched — and fetched successfully — rather than assuming crawlability from configuration alone.

---

# robots.txt

`robots.txt` provides crawl instructions for automated agents.

A simple example:

```text
User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml
```

Adapt the rules to the actual website.

> `robots.txt` is not an access-control mechanism. Private information should be protected through authentication and authorization.

### Common robots.txt Considerations for 3D Tool Sites

* Decide deliberately whether AI crawlers should be allowed or disallowed — different AI companies publish different user-agent tokens, and policy here is a business decision, not just a technical one.
* Avoid accidentally disallowing JavaScript or CSS asset paths, which can prevent search engines from rendering the page correctly even if the HTML itself is allowed.
* Keep user-generated or duplicate routes (e.g. temporary upload previews) out of the crawl path if they don't provide standalone value.

---

# sitemap.xml

XML sitemaps help search engines discover important URLs.

For a 3D website, sitemap entries may include:

* Homepage
* Tool pages
* Product pages
* Documentation
* Tutorials
* Guides
* Category pages
* Public model pages

Avoid adding URLs that should not be indexed.

### Keeping Sitemaps Healthy

* Regenerate the sitemap automatically as part of the build process rather than maintaining it by hand, so new tool or guide pages are never missed.
* Include `lastmod` dates so crawlers can prioritize recently updated content.
* Split very large sitemaps (thousands of URLs, e.g. a large public model gallery) into a sitemap index referencing multiple smaller sitemap files.

---

# llms.txt

`llms.txt` is an emerging convention intended to provide information about a website for language-model systems.

It should not be treated as a replacement for:

* HTML
* robots.txt
* sitemap.xml
* Structured data
* Metadata
* Good technical SEO

If you use `llms.txt`, keep it useful, concise, and maintained.

Because this is an emerging and not-yet-standardized convention, treat any `llms.txt` implementation as an experiment layered on top of a technically sound site rather than a substitute for one — support for it varies across AI systems and is likely to keep evolving.

---

# Metadata & Open Graph

Important pages should have useful metadata.

Common elements include:

* `<title>`
* Meta description
* Canonical URL
* Open Graph metadata
* Social preview metadata
* Robots directives
* Language metadata

### Example

```html
<title>GLB Viewer – View 3D Models Online</title>
```

A title such as:

```text
Home
```

provides much less context.

Metadata should clearly communicate the purpose of the page.

### Open Graph for 3D Tool Pages

Because 3D tool pages are frequently shared on social platforms, Discord, and developer forums, a well-configured `og:image` (a static preview render or screenshot of the tool in use) and `og:description` meaningfully affect click-through from shared links. Where feasible, generate a dynamic Open Graph image per model or tool state (e.g. via an edge function) so shared links show the actual content rather than a generic placeholder.

---

# Analytics

Analytics can help developers understand how users interact with 3D applications.

Useful events may include:

* Model uploaded
* Model loaded
* Screenshot created
* Tool opened
* Format selected
* Download started
* Viewer interaction
* Error encountered
* Conversion completed

Only collect data that is necessary and appropriate for the product.

### Turning Analytics Into SEO/GEO Decisions

Beyond product analytics, funneling this event data into decisions about which tool pages to expand, which FAQs to add, and which formats to prioritize supporting next closes the loop between what users actually search for/do and what content gets built — rather than guessing at content priorities.

---

# Search Console Tools

Useful search and indexing tools include:

* Google Search Console
* Bing Webmaster Tools
* URL inspection tools
* Rich result testing tools
* Search analytics
* Indexing reports
* Crawl reports

For 3D websites, investigate:

* Indexed pages
* Crawled pages
* Rendering issues
* Mobile usability
* Core Web Vitals
* Structured data
* Search queries
* Page indexing

### A Simple Weekly Search Console Routine

* Check the Pages report for any new "Crawled – currently not indexed" or "Discovered – currently not indexed" entries and investigate why.
* Spot-check a sample of tool pages with the URL Inspection tool to confirm rendered HTML actually includes the important text content, not just the canvas shell.
* Watch the Core Web Vitals report for regressions after any 3D asset or dependency update.

* [CrakSEO Search Console MCP](https://docs.crakseo.com/mcp-servers/search-console) - Free remote MCP access for an AI assistant to check owned-site search-query/page performance and URL inspection during this routine; CrakSEO authentication and property authorization required. It does not render or inspect 3D assets.

---

# Developer Tools

## Browser DevTools

Useful for inspecting:

* HTML
* CSS
* JavaScript
* Network requests
* Performance
* Memory
* WebGL
* WebGPU

## Lighthouse

Useful for auditing:

* Performance
* Accessibility
* Best practices
* SEO

## PageSpeed Insights

Useful for investigating:

* Performance
* Core Web Vitals
* Mobile performance
* Desktop performance

## WebPageTest

Useful for detailed loading and performance analysis.

## Chrome DevTools

Useful for debugging:

* Rendering
* Network behavior
* JavaScript execution
* Memory
* Performance
* GPU-related behavior

### Three.js/WebGL-Specific Debugging Tools

Beyond general browser DevTools, dedicated WebGL/Three.js inspectors (such as browser extensions built specifically for inspecting Three.js scene graphs, draw calls, and GPU memory) are worth adding to a regular debugging routine, since generic DevTools performance panels don't always surface scene-graph-level issues like redundant materials or excessive draw calls.

---

# Learning Resources

## SEO

Learn the fundamentals first:

* Search intent
* Crawling
* Indexing
* Ranking
* Technical SEO
* Internal linking
* Structured data
* Site architecture
* Content quality

## AI Search

Useful topics include:

* Information retrieval
* Retrieval systems
* Embeddings
* Entity understanding
* Knowledge graphs
* AI-generated answers
* Citation systems
* Search quality

## GEO

Explore:

* Content discoverability
* Entity clarity
* Information retrieval
* Source authority
* Structured information
* AI answer generation

## 3D Web

Learn:

* Three.js
* React Three Fiber
* WebGL
* WebGPU
* glTF
* GLB
* PBR
* GPU optimization
* Texture compression
* Web performance

---

# 3D Web Resources

## Three.js

JavaScript 3D library for creating interactive 3D experiences on the web.

Useful for:

* WebGL applications
* Product visualization
* 3D websites
* Interactive experiences
* Data visualization

## React Three Fiber

A React renderer for Three.js.

Useful for:

* React applications
* 3D interfaces
* Product configurators
* Interactive experiences

## Babylon.js

A JavaScript framework for building 3D applications.

Useful for:

* Games
* Simulations
* WebXR
* Product experiences

## glTF

A modern 3D transmission format designed for efficient delivery and rendering.

Common formats:

* `.gltf`
* `.glb`

## WebGL

A browser API for hardware-accelerated graphics.

## WebGPU

A modern graphics and compute API for the web.

### Choosing Between Three.js and Babylon.js

Both libraries solve overlapping problems, but they lean differently in practice: Three.js has a larger community, more third-party tutorials, and a lighter core, which tends to suit product viewers, portfolio sites, and content-heavy 3D websites. Babylon.js ships more built-in engine features (physics, WebXR tooling, a visual scene editor) out of the box, which tends to suit games and more application-like 3D experiences. Neither choice inherently helps or hurts SEO — the surrounding architecture matters far more than the rendering library itself.

---

# Recommended 3D Web Architecture

A strong 3D website separates information from rendering.

```text
3D Website
│
├── SEO Layer
│   ├── Metadata
│   ├── Semantic HTML
│   ├── Structured Data
│   ├── Internal Links
│   └── Content
│
├── Discovery Layer
│   ├── robots.txt
│   ├── sitemap.xml
│   ├── Canonicals
│   └── Crawler considerations
│
├── Performance Layer
│   ├── Image optimization
│   ├── GLB optimization
│   ├── Texture compression
│   ├── Code splitting
│   └── Lazy loading
│
└── 3D Layer
    ├── Three.js
    ├── React Three Fiber
    ├── WebGL / WebGPU
    ├── GLB / glTF
    └── Interactive Experience
```

This separation makes the application easier to maintain and gives machines more useful information to work with.

Treat these four layers as a dependency order, not just a conceptual grouping: the SEO and Discovery layers should be functional even if the 3D layer fails to load entirely (e.g. on a browser without WebGL support, or if a script fails to fetch). A page that degrades gracefully to a fully readable HTML page — with a fallback image in place of the canvas — is both more resilient for users and easier for crawlers to fully understand.

---

# 3D E-commerce SEO

3D e-commerce websites have additional opportunities.

A product page can combine:

```text
Product Information
        +
Product Images
        +
Interactive 3D Model
        +
Specifications
        +
Structured Data
        +
Reviews
        +
FAQ
        +
Related Products
```

The 3D model should enhance the product page rather than replace product information.

Important product information should remain available as normal HTML.

### Why 3D Product Pages Can Outperform Static Ones

An interactive 3D viewer on a product page tends to improve on-page engagement metrics (time on page, interaction rate) when it's layered on top of — rather than instead of — complete written product information. Search engines don't directly reward "having a 3D viewer," but the engagement and reduced return/refund rates it can produce are indirect business benefits worth measuring alongside the SEO fundamentals covered elsewhere in this document.

---

# 3D Tool Website SEO

3D tools can benefit from dedicated landing pages.

For example:

```text
/3d-model-viewer
/glb-viewer
/gltf-viewer
/3d-model-screenshot
/glb-screenshot
```

Each page can target a specific user intent while providing:

* Tool description
* Supported formats
* Features
* How it works
* Examples
* FAQs
* Documentation
* Related tools

This creates useful entry points for users and search systems.

### Avoiding Keyword Cannibalization Between Tool Pages

When a site offers multiple closely related tools (e.g. a GLB viewer and a glTF viewer), give each page a distinct primary intent and avoid duplicating large blocks of copy between them — otherwise search engines may struggle to decide which page to rank for a given query, diluting both. Link the pages to each other explicitly ("Looking for glTF support? Try our glTF Viewer") rather than letting users or crawlers guess the relationship.

---

# Example SEO Checklist for a 3D Tool

```text
[ ] Unique page title
[ ] Useful meta description
[ ] Canonical URL
[ ] Semantic HTML
[ ] One clear H1
[ ] Descriptive headings
[ ] Helpful page content
[ ] Internal links
[ ] Structured data where appropriate
[ ] Optimized images
[ ] Optimized 3D assets
[ ] Mobile-friendly experience
[ ] Fast initial page load
[ ] Crawlable URLs
[ ] Valid sitemap
[ ] Correct robots.txt
[ ] Useful Open Graph metadata
[ ] Accessible non-WebGL content
[ ] Error handling
```

---

# How to Use This Repository

This repository is designed as a practical reference rather than a strict course.

If you are new to 3D Web SEO, a useful learning order is:

```text
1. SEO Fundamentals
        ↓
2. Technical SEO
        ↓
3. JavaScript / WebGL SEO
        ↓
4. Structured Data
        ↓
5. Web Performance
        ↓
6. 3D Model SEO
        ↓
7. AI Search
        ↓
8. AEO
        ↓
9. GEO
        ↓
10. AI Overviews & Answer Engines
```

You do not need to implement everything at once.

Start with a technically sound website and improve it step by step.

---

# Recommended Workflow

## 1. Build the page

Create useful HTML content first.

## 2. Add the 3D experience

Use Three.js, React Three Fiber, Babylon.js, or another suitable technology.

## 3. Optimize assets

Optimize:

* GLB
* glTF
* Textures
* Images
* JavaScript
* Fonts

## 4. Add technical SEO

Implement:

* Metadata
* Canonicals
* Sitemap
* Robots
* Internal linking

## 5. Add structured data

Use schema types that accurately describe the page.

## 6. Test performance

Measure:

* Core Web Vitals
* JavaScript execution
* Network loading
* 3D loading
* Rendering performance

## 7. Improve AI discoverability

Make important entities, facts, relationships, and explanations easy to understand.

## 8. Monitor

Use analytics and search tools to understand how the website performs.

---

# Common Mistakes

### Making the entire website a canvas

A WebGL experience does not automatically communicate useful information to search engines or AI systems.

### Rendering everything client-side

Heavy client-side rendering can make initial content and crawling more difficult.

### Ignoring performance

A technically correct website can still provide a poor experience when the 3D scene is too expensive.

### Hiding product information inside the model

Important specifications should not exist only inside the 3D scene.

### Using structured data incorrectly

Structured data should accurately describe relevant page content.

### Blocking useful crawlers accidentally

Review robots directives before deploying them.

### Focusing only on keywords

Modern search involves intent, entities, context, quality, usefulness, and technical accessibility.

### Treating GEO/AEO as separate from SEO

Generative and answer engines still rely heavily on crawlability, structured content, and clear entity information — the same foundations as traditional SEO. Treating GEO as an entirely separate discipline with its own unrelated checklist often leads teams to neglect the technical basics that both traditional and AI-driven discovery depend on.

### Skipping mobile testing for 3D content specifically

A page can pass general mobile-usability checks while still performing poorly once the 3D scene actually loads on a mid-range mobile GPU. Test the fully-loaded 3D experience on real mobile hardware, not just the surrounding HTML.

---

# Frequently Asked Questions

## What is GEO?

GEO generally refers to **Generative Engine Optimization**: improving content so generative search and AI systems can discover, understand, retrieve, and potentially reference it.

## What is AEO?

AEO generally refers to **Answer Engine Optimization**, focusing on creating content that directly satisfies questions in answer-oriented search systems.

## What are AI Overviews?

AI Overviews are AI-generated summaries that can appear within search experiences and provide synthesized information from multiple sources.

## Is GEO a replacement for SEO?

No.

Technical SEO, useful content, accessibility, structured information, and good site architecture remain important foundations.

## Does Three.js hurt SEO?

Three.js itself does not automatically hurt SEO.

The bigger factor is how the website is architected around the 3D experience.

## Should important text be inside WebGL?

Generally, no.

Important information should be available as normal HTML whenever practical.

## Can a 3D website rank in search?

Yes.

A 3D website can rank when it provides useful content, is technically crawlable, has good information architecture, and satisfies user intent.

## Should every 3D model have its own page?

Not necessarily.

Create dedicated pages when they provide meaningful value and represent distinct content or search intent.

## Is llms.txt required for AI SEO?

There is no universal requirement to use it.

Treat it as an emerging convention rather than a replacement for established web standards and SEO fundamentals.

## Should I optimize GLB files for SEO?

GLB optimization primarily improves performance rather than directly improving rankings.

However, better performance can improve the overall user experience.

## Does image alt text help 3D model SEO?

Descriptive alt text can improve accessibility and help communicate the purpose of meaningful images.

## Should 3D websites use structured data?

When applicable, yes.

Use structured data that accurately describes the page and its visible content.

## How long does 3D website SEO take to show results?

As with most SEO work, timelines vary widely by competition, domain age, and content quality, but meaningful indexing and ranking movement for a new site is typically measured in months rather than days or weeks — technical fixes (crawlability, indexability) tend to show effects fastest, while content and authority-driven ranking gains take longer.

## Do AI crawlers respect robots.txt the same way search engines do?

Not universally — different AI companies have published different crawler user-agents with varying levels of documented respect for robots.txt directives, and this landscape continues to change. Review each crawler's published behavior rather than assuming uniform treatment.

---

# 3D Web SEO Checklist

```text
Technical
├── Crawlable
├── Indexable
├── Canonical
├── Sitemap
├── Robots
└── Correct HTTP status codes

Content
├── Clear topic
├── Search intent
├── Semantic HTML
├── Useful headings
├── Internal links
└── Helpful supporting content

AI Search
├── Clear entities
├── Clear relationships
├── Factual information
├── Structured information
├── Helpful answers
└── Strong source context

3D
├── Optimized GLB / glTF
├── Optimized textures
├── Efficient geometry
├── Lazy loading
├── Code splitting
└── GPU-conscious rendering

Performance
├── Core Web Vitals
├── JavaScript
├── Images
├── Fonts
├── Network
└── 3D loading

Metadata
├── Title
├── Description
├── Canonical
├── Open Graph
└── Structured Data
```

---

# Contributing

Contributions are welcome.

This repository is intended to become a practical reference for developers building modern 3D websites.

You can contribute by:

* Adding useful AI tools
* Adding 3D development resources
* Adding SEO documentation
* Adding GEO resources
* Adding AEO resources
* Adding AI search resources
* Adding performance tools
* Adding structured data resources
* Improving descriptions
* Fixing broken links
* Removing outdated resources
* Adding useful tutorials
* Improving organization
* Reporting incorrect information

## Contribution Guidelines

Before submitting a contribution:

* Prefer official documentation.
* Prefer actively maintained projects.
* Avoid duplicate entries.
* Keep descriptions concise.
* Explain why a resource is useful.
* Avoid promotional descriptions.
* Verify links before submitting.
* Keep categories focused.
* Do not add unrelated resources.

Please read `CONTRIBUTING.md` before opening a Pull Request.

---

# Support

If this repository is useful to you:

* ⭐ Star the repository
* 🍴 Fork it
* 📢 Share it with other developers
* 💡 Submit useful resources
* 🐛 Report broken or outdated information
* 🔧 Contribute improvements

The goal is to build a practical resource that helps developers make the modern 3D Web more **discoverable, performant, accessible, and understandable**.

---

# Related GLBKit Resources

[GLBKit](https://glbkit.com/) is a browser-based collection of tools for working with 3D assets.

Useful tools include:

* 3D Model Viewer
* GLB Viewer
* 3D Model Screenshot
* GLB Screenshot
* 3D Model Information
* 3D asset inspection tools

Visit:

**https://glbkit.com/**

---

# License

This project is dedicated to the public domain under the **Creative Commons CC0 1.0 Universal (CC0 1.0) Public Domain Dedication**.

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

See the `LICENSE` file for the full license text.

---

## Made for the 3D Web Community

Built for developers working with:

**Three.js · React Three Fiber · WebGL · WebGPU · glTF · GLB · AI · SEO · GEO · AEO · AI Search · 3D E-commerce · 3D Tools**

If you are building the next generation of 3D websites, this list is for you. 🌐
