# HTML Standard FAQ

_See also the [WHATWG FAQ](https://whatwg.org/faq)._

## HTML

### What is HTML?

[HTML](https://html.spec.whatwg.org/multipage/) is one of the standards being worked on by the WHATWG community. It is a new version of HTML4, XHTML1, and DOM Level 2 HTML addressing many of the issues of those specifications while at the same time enhancing (X)HTML to more adequately address Web applications. Besides defining a markup language that can be written in both HTML and XML (XHTML) it also defines many APIs that form the basis of the Web architecture. Some of these APIs were known as "DOM Level 0" and were never documented before, yet are extremely important for browser vendors to support existing Web content and for authors to be able to build Web applications.

### What is HTML5?

Going forward, the WHATWG is just working on "HTML", without worrying about version numbers. When people talk about HTML5 in the context of the WHATWG, they usually mean just "the latest work on HTML", not necessarily a specific version. For more details, see the section called "[Is this HTML5?](https://html.spec.whatwg.org/multipage/introduction.html#is-this-html5?)" in the specification.

### How do I validate my pages?

Use a [validator](https://whatwg.org/validator/).

### What parts of the specification are stable?

The whole specification is more or less stable except where there are big messages pointing out some unresolved issue. (These are pretty rare.) There are some parts of the spec that describe new technology that has not yet been implemented, but at this point these additions are only added after the design itself is pretty stable.

(In practice, implementations all follow the latest specification drafts anyway, not so-called "finished" snapshots. The problem with following a snapshot is that you end up following something that is _known to be wrong_. That's obviously not the way to get interoperability! This has in fact been a real problem at the W3C, where mistakes are found and fixed in the editors' drafts of specifications, but implementors who aren't fully engaged in the process go and implement obsolete snapshots instead, including those bugs, without realising the problems, and resulting in differences between the browsers.)

### Will future browsers have any idea what older HTML documents mean?

Browsers do not implement HTML+, HTML2, HTML3.2 HTML4, HTML4.01, etc, as separate versions. They all just have a single implementation that covers all these versions at once. That is what the WHATWG HTML specification defines: how to write a browser (or other implementation) that handles _all previous versions of HTML_, as well as all the latest features.

One of the main goals of the HTML specification and the WHATWG effort as a whole is to make it possible for archeologists hundreds of years from now to write a browser and view HTML content, regardless of when it was written. Making sure that we handle all documents is one of our most important goals. Not having versions does not preclude this; indeed it makes it significantly easier.

### How are developers to determine when certain parts of their pages will become invalid?

It shouldn't matter if and when old pages become invalid.

Validity (more often referred to as document conformance in the WHATWG) is a quality assurance tool to help authors avoid mistakes. We don't make things non-conforming (invalid) for the sake of it, we use conformance as a guide for developers to help them avoid bad practices or mistakes (like typos). So there's not really any need to worry about whether old pages are conforming or not, it's only helpful when you're writing a new page, and it's always most helpful to have the latest advice. It wouldn't be useful to check for compliance against last week's rules, for instance. After all, we fixed mistakes in those rules this week! For more details, see [part of the introduction](https://html.spec.whatwg.org/multipage/introduction.html#conformance-requirements-for-authors) of the specification.

### How can I keep track of changes to the spec?

There are a number of ways to track changes to the spec:

* The Twitter feed: [@htmlstandard](https://twitter.com/htmlstandard)
* The [GitHub commits log](https://github.com/whatwg/html/commits/master)
* The specification is available in the [Git repository](https://github.com/whatwg/html/). You may use any Git client to check out the latest version and use your client's diff tools to compare revisions and see what has been changed.
* At a broader level, Anne and Simon once wrote a document that gave a high-level overview of changes to HTML over the last decade or so: https://html-differences.whatwg.org/

### What are the various versions of the HTML spec?

The HTML Standard is available in two forms: [single-page](https://html.spec.whatwg.org/) (_very large_) and [multi-page](https://html.spec.whatwg.org/multipage/).

The WHATWG [also works on other standards](https://spec.whatwg.org/), such as the DOM, URL, and XMLHttpRequest standards.

The W3C publishes some forked versions of these specifications. We have requested that they stop publishing these but they have refused. They copy most of our fixes into their forks, but their forks are usually weeks to months behind. They also make intentional changes, and sometimes even unintentional changes, to their versions. We highly recommend not paying any attention to the W3C forks of WHATWG standards.

### Are there versions of the HTML specification aimed specifically at authors/implementors?

Yes! https://html.spec.whatwg.org/dev/

### When will we be able to start using these new features?

You can use some of them now. Others might take a few more years to get widely implemented. Here are some sites to help you work out what you can use:

* http://diveintohtml5.info/
* http://caniuse.com/
* http://html5doctor.com/
* https://developer.mozilla.org/

If you know of any more (or if you have some yourself) then add them to the list! If there are some on the list that aren't very useful compared to the rest, then remove them!

### When will HTML5 be finished?

The WHATWG is now using a Living Standard development model, so this question is no longer really pertinent. See above, under "[What is HTML5?](#what-is-html5)". The real question is, when can you use new features? For an answer to that question, see "[When will we be able to start using these new features?](#when-will-we-be-able-to-start-using-these-new-features)".

### What's this I hear about 2022?

Before the WHATWG transitioned to an unversioned model for HTML, when we were still working on HTML5 and still thought in terms of snapshot drafts reaching milestones as a whole rather than on a per-section basis, the editor estimated that we'd reach Last Call in October 2009, Candidate Recommendation in the year 2012, and Recommendation in the year 2022 or later. This would be approximately 18-20 years of development, since beginning in mid-2004, which is on par with the amount of work that other specs of similar size and similar maturity receive to get to the same level of quality. For instance, it's in line with the timeline of CSS2/2.1. Compared to HTML4's timetable it may seem long, but consider: work on HTML4 started in the mid 90s, and HTML4 _still_, more than ten years later, hadn't reached the level that we want to reach with HTML now. There was no real test suite, there are many parts of the HTML4 spec that are lacking real implementations, there are big parts of HTML4 that aren't interoperable, and the HTML4 spec has hundreds if not thousands of known errors that haven't been fixed. When HTML4 came out, REC meant something much less exciting than the WHATWG is aiming for. We now look for two 100% complete and fully interoperable implementations, which is proven by each successfully passing literally thousands of test cases (20,000 tests for the whole spec would probably be a conservative estimate). When you consider how long it takes to write that many test cases and how long it takes to implement each feature, you'll begin to understand why the time frame seems so long.

Now that we've moved to a more incremental model without macro-level milestones, the 2022 date is no longer relevant.

### What about Microsoft and Internet Explorer?

Microsoft started implementing new parts of the contemporary HTML standard in IE8 and has been adding more to IE since.

HTML is being developed with compatibility with existing browsers in mind, though (including IE). Support for many features can be simulated using JavaScript.

### Is design rationale documented?

Sort of. Often the documentation can be found in the mailing list or IRC channel archives. Sometimes an issue was raised formally, and resolution is recorded in the issue tracker. Sometimes, there is an explanation in the specification, but doing that everywhere would make the specification huge.

For a few cases that someone did take the time document, the information can be found at the following locations:

* [Rationale](https://wiki.whatwg.org/wiki/Rationale) — a page that documents some reasons behind decisions in the spec, originally written and maintained by Variable. If anyone wants to help him out, try to grab someone on [IRC](https://wiki.whatwg.org/wiki/IRC) (e.g. Hixie), we're always looking for more contributors and this is a good place to start.
* [Why no namespaces](https://wiki.whatwg.org/wiki/Why_no_namespaces)
* [Why no script implements](https://wiki.whatwg.org/wiki/Why_no_script_implements)
* [Why not reuse legend](https://wiki.whatwg.org/wiki/Why_not_reuse_legend) or another _mini-header_ element.

Also see _HTML feature proposals_ below.

## HTML syntax issues

### Will HTML finally put an end to the XHTML as `text/html` debate?

Yes. Unlike HTML4 and XHTML1, the choice of HTML or XHTML is solely dependent upon the choice of the media type, rather than the DOCTYPE. See [HTML vs. XHTML](https://wiki.whatwg.org/wiki/HTML_vs._XHTML)

### What is the DOCTYPE for modern HTML documents?

In HTML:

```html
<!DOCTYPE html>
```

In XHTML: no DOCTYPE is required and its use is generally unnecessary. However, you may use one if you want (see the following question). Note that the above is well-formed XML and so it may also appear in XHTML documents.

For compatibility with legacy producers designed for outputting HTML, but which are unable to easily output the above DOCTYPE, this alternative legacy-compat version may be used instead.

```html
<!DOCTYPE html SYSTEM "about:legacy-compat">
```

Note that this is _not_ intended for dealing with any compatibility issues with legacy browsers. It is meant for legacy authoring tools only.

Excluding the string `"about:legacy-compat"`, the DOCTYPE is case insensitive in HTML. In XHTML, it is case sensitive and must be either of the two variants given above. For this reason, the DOCTYPEs given above are recommended to be used over other case variants, such as `<!DOCTYPE HTML>` or `<!doctype html>`.

These alternatives were chosen because they meet the following criteria:

* They trigger standards mode in all current and all relevant legacy browsers.
* They are well-formed in XML and can appear in XHTML documents.
* It is possible to output at least one of the alternatives, if not both, with extant markup generators.
* They intentionally contain no language version identifier so the DOCTYPE will remain usable for all future revisions of HTML.
* The first is short and memorable to encourage its use.
* The legacy-compat DOCTYPE is intentionally unattractive and self descriptive of purpose to discourage unnecessary use.

### Under what conditions should a DOCTYPE be used in XHTML?

Generally, the use of a DOCTYPE in XHTML is unnecessary. However, there are cases where inclusion of a DOCTYPE is a reasonable thing to do:

1. The document is intended to be a polyglot document that may be served as both HTML or XHTML.
2. You wish to declare entity references for use within the document. Note that most browsers only read the internal subset and do not retrieve external entities. (This is not compatible with HTML, and thus not suitable for polyglot documents.)
3. You wish to use a custom DTD for DTD-based validation. But take note of [what's wrong with DTDs](https://about.validator.nu/#faq).

Fundamentally, this is an XML issue, and is not specific to XHTML.

### How are documents from HTML4 and earlier versions parsed?

All documents with a text/html media type (that is, including those without or with an HTML 2.0, HTML 3.2, HTML4, or XHTML1 DOCTYPE) will be parsed using the same parser algorithm as defined by the HTML spec. This matches what Web browsers have done for HTML documents so far and keeps code complexity down. That in turn is good for security, maintainability, and in general keeping the amount of bugs down. The HTML syntax as now defined therefore does not require a new parser and documents with an HTML4 DOCTYPE for example will be parsed as described by the new HTML specification.

Validators are allowed to have different code paths for previous levels of HTML.

### If there is no DTD, how can I validate my page?

With an [HTML validator](https://whatwg.org/validator/) that follows the latest specification.

### What is an HTML Serialization?

The HTML serialization refers to the syntax of an HTML document defined in the HTML specification. The syntax is inspired by the SGML syntax from earlier versions of HTML, bits of XML (e.g. allowing a trailing slash on void elements, `xmlns` attributes), and reality of deployed content on the Web.

Any document whose MIME type is determined to be `text/html` is considered to be an HTML serialization and must be parsed using an HTML parser.

### What is an XML (or XHTML) Serialization?

The XML Serialization refers to the syntax defined by XML 1.0 and Namespaces in XML 1.0. A resource that has an XML MIME type, such as `application/xhtml+xml` or `application/xml`, is an XML document and if it uses elements in the HTML namespace, it contains XHTML. If the root element is `html` in the HTML namespace, the document is referred to as an XHTML document.

### What MIME type does HTML use?

The HTML serialization _must_ be served using the `text/html` MIME type.

The XHTML serialization _must_ be served using an XML MIME type, such as `application/xhtml+xml` or `application/xml`. Unlike the situation as of XHTML1, the HTML specification says that XHTML must no longer be served as `text/html`.

Using the incorrect MIME type (`text/html`) for XHTML will cause the document to be parsed according to parsing requirements for HTML. In other words, it will be treated as tag soup. Ensuring the use of an XML MIME type is the only way to ensure that browsers handle the document as XML.

### Should I close empty elements with `/>` or `>`?

Void elements in HTML (e.g. the `br`, `img` and `input` elements) do not require a trailing slash. e.g. Instead of writing `<br />`, you only need to write `<br>`. This is the same as in HTML4. However, due to the widespread attempts to use XHTML1, there are a significant number of pages using the trailing slash. Because of this, the trailing slash syntax has been permitted on void elements in HTML in order to ease migration from XHTML1 back to HTML.

The new HTML specification also introduces the ability to embed MathML elements. On elements inside a `math` element the trailing slash works just like it does in XML. I.e. it closes the element. This is only inside that context however, it does not work for normal HTML elements.

### If I'm careful with the syntax I use in my HTML document, can I process it with an XML parser?

Yes. Find guidance in [HTML vs. XHTML](https://wiki.whatwg.org/wiki/HTML_vs._XHTML#Differences_Between_HTML_and_XHTML) and [Polyglot Markup: HTML-Compatible XHTML Documents](https://dev.w3.org/html5/html-polyglot/html-polyglot.html).

A word of warning though. You have to be _really_ careful for this to work, and it's almost certainly not worth it. You'd be better off just using an HTML-to-XML parser. That way you can just use HTML normally while still using XML pipeline tools.

### What is the namespace declaration?

In XHTML, you are required to specify the namespace:

```html
<html xmlns="http://www.w3.org/1999/xhtml">
```

In HTML, the `xmlns` attribute is currently allowed on any HTML element, but only if it has the value `http://www.w3.org/1999/xhtml`. It doesn't do anything at all, it is merely allowed to ease migration from XHTML1. It is not actually a namespace declaration in HTML, because HTML doesn't yet support namespaces. See the question "[Will there be support for namespaces in HTML?](#will-there-be-support-for-namespaces-in-html)".

### Will there be support for namespaces in HTML?

HTML is being defined in terms of the DOM and during parsing of a text/html all HTML elements will be automatically put in the HTML namespace, `http://www.w3.org/1999/xhtml`. However, unlike the XHTML serialization, there is no real namespace syntax available in the HTML serialization (see previous question). In other words, you do not need to declare the namespace in your HTML markup, as you do in XHTML. However, you are permitted to put an `xmlns` attribute on each HTML element as long as the namespace is `http://www.w3.org/1999/xhtml`.

In addition, the HTML syntax provides for a way to embed elements from MathML and SVG. Elements placed inside the container element `math` or `svg` will automatically be put in the MathML namespace or the SVG namespace, respectively, by the parser. Namespace syntax is not required, but again an `xmlns` attribute is allowed if its value is the right namespace.

In conclusion, while HTML does not allow the XML namespace syntax, there is a way to embed MathML and SVG and the `xmlns` attribute can be used on any element under the given constraints, in a way that is reasonably compatible on the DOM level.

### How do I specify the character encoding?

For HTML, it is strongly recommended that you specify the encoding using the HTTP `Content-Type` header. If you are unable to [configure your server](http://www.w3.org/International/O-HTTP-charset) to send the correct headers, then you may use the `meta` element:

```html
<meta charset="UTF-8">
```

The following restrictions apply to character encoding declarations:

* The character encoding name given must be the name of the character encoding used to serialize the file.
* The value must be a [valid character encoding name](http://www.iana.org/assignments/character-sets), and must be the preferred name for that encoding.
* The character encoding declaration must be serialized without the use of character references or character escapes of any kind.
* The `meta` element used for this purpose must occur within the first 512 bytes of the file. It is considered good practice for this to be the first child of the `head` element so that it is as close to the beginning of the file as possible.

Note that this `meta` element is different from HTML 4, though it is compatible with many browsers because of the way encoding detection has been implemented.

For polyglot documents, which may be served as either HTML or XHTML, you may also include that in XHTML documents, but only if the encoding is UTF-8.

To ease transition from HTML4 to the latest HTML specification, although the former is the recommended syntax, you may also use the following. (This does not apply to XHTML or polyglot documents)

```html
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
```

In XHTML, XML rules for determining the character encoding apply. The meta element is never used for determining the encoding of an XHTML document (although it may appear in UTF-8 encoded XHTML documents). You should use either the HTTP `Content-Type` header or the XML declaration to specify the encoding.

```html
<?xml version="1.0" encoding="UTF-8"?>
```

Otherwise, you must use the default of `UTF-8` or `UTF-16`. It is recommended that you use `UTF-8`.

### What are the differences between HTML and XHTML?

See the list of [differences between HTML and XHTML](https://wiki.whatwg.org/wiki/HTML_vs._XHTML#Differences_Between_HTML_and_XHTML) in the wiki.

### What are best practices to be compatible with HTML DOM and XHTML DOM?

Though the intent is that HTML and XHTML can both produce identical DOMs, there still are some differences between working with an HTML DOM and an XHTML one.

Case sensitivity:

* Whenever possible, avoid testing Element.tagName and Node.nodeName (or do toLowerCase() before testing).

Namespaces:

* Use the namespace-aware version for creating elements: Document.createElementNS(ns, elementName)

### Why does this new HTML spec legitimise tag soup?

Actually it doesn't. This is a misconception that comes from the confusion between conformance requirements for documents, and the requirements for user agents.

Due to the fundamental design principle of supporting existing content, the spec must define how to handle all HTML, regardless of whether documents are conforming or not. Therefore, the spec defines (or will define) precisely how to handle and recover from erroneous markup, much of which would be considered tag soup.

For example, the spec defines algorithms for dealing with syntax errors such as incorrectly nested tags, which will ensure that a well structured DOM tree can be produced.

Defining that is essential for one day achieving interoperability between browsers and reducing the dependence upon reverse engineering each other.

However, the conformance requirements for authors are defined separately from the processing requirements. Just because browsers are required to handle erroneous content, it does not make such markup conforming.

For example, user agents will be required to support the marquee element, but authors must not use the marquee element in conforming documents.

It is important to make the distinction between the rules that apply to user agents and the rules that apply to authors for producing conforming documents. They are completely orthogonal.

## HTML feature proposals

### HTML should support `href` on any element!

The spec allows `<a>` to contain blocks. It doesn't support putting `href=""` on any element, though.

Supporting `href` on any element has several problems associated with it that make it difficult to support in HTML. The main reason this isn't in HTML is that browser vendors have reported that implementing it would be extremely complex. Browser vendors get to decide what they implement, and there's no point to us telling them to do something they aren't going to do. In addition:

* It isn't backwards compatible with existing browsers.
* It adds no new functionality that can't already be achieved using the `a` element and a little script.
* It doesn't make sense for all elements, such as interactive elements like `input` and `button`, where the use of href would interfere with their normal function.

The only advantage it seems to add is that it reduces typing for authors in some cases, but that is not a strong enough reason to support it in light of the other reasons.

Wrapping `<a>` elements around blocks solves most use cases. It doesn't handle making rows in tables into links, though; for those just do something like this instead:

```html
<tr onclick="location = this.getElementsByTagName('a')[0]"> ... </tr>
```

### HTML should support list headers!

You can give a header to a list using the `<figure>` and `<figcaption>` elements:

```html
<figure>
 <figcaption>Apples</figcaption>
 <ul>
  <li>Granny Smith</li>
  <li>Evil Apple of Knowledge</li>
  <li>Apple, Inc</li>
 </ul>
</figure>
```

You can also label a group of lists using a definition list:

```html
<dl>
 <dt>Dry:</dt>
 <dd>
  <ul>
   <li>1c flour</li>
   <li>1/4c sugar</li>
   <li>1tsp baking soda</li>
  </ul>
 </dd>
 <dt>Wet:</dt>
 <dd>
  <ul>
   <li>1 egg </li>
   <li>1/2c milk</li>
   <li>1tsp vanilla extract</li>
  </ul>
 </dd>
</dl>
```

These techniques are preferred over adding an `<lh>` element as proposed in the old HTML3 draft, mostly because of thorny issues with parsing near `<li>` elements.

### HTML should support a way for anyone to invent new elements!

There are actually quite a number of ways for people to invent their own extensions to HTML:

* Authors can use the `class` attribute to extend elements, effectively creating their own elements, while using the most applicable existing "real" HTML element, so that browsers and other tools that don't know of the extension can still support it somewhat well. This is the tack used by Microformats, for example.
* Authors can include data for scripts to process using the `data-*=""` attributes. These are guaranteed to never be touched by browsers, and allow scripts to include data on HTML elements that scripts can then look for and process.
* Authors can use the `<meta name="" content="">` mechanism to include page-wide metadata. Names should be registered on the wiki's [MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions) page.
* Authors can use the `rel=""` mechanism to annotate links with specific meanings. This is also used by Microformats. Names should be registered on the wiki's [RelExtensions](https://wiki.whatwg.org/wiki/RelExtensions) page.
* Authors can embed raw data using the `<script type="">` mechanism with a custom type, for further handling by a script.
* Authors can create plugins and invoke them using the `<embed>` element. This is how Flash works.
* Authors can extend APIs using the JS prototyping mechanism. This is widely used by script libraries, for instance.
* Authors can use the microdata feature (the `item=""` and `itemprop=""` attributes) to embed nested name-value pairs of data to be shared with other applications and sites.
* Authors can use [custom elements](https://html.spec.whatwg.org/multipage/custom-elements.html).
* Authors can propose new elements and attributes to the working group and, if the wider community agrees that they are worth the effort, they are added to the language. (If an addition is urgent, please let us know when proposing it, and we will try to address it quickly.)

There is currently no mechanism for introducing new proprietary features in HTML documents (i.e. for introducing new elements and attributes) without discussing the extension with user agent vendors and the wider Web community. This is intentional; we don't want user agents inventing their own proprietary elements and attributes like in the "bad old days" without working with interested parties to make sure their feature is well designed.

We request that people not invent new elements and attributes to add to HTML without first contacting the working group and getting a proposal discussed with interested parties.

### HTML should group `<dt>`s and `<dd>`s together in `<di>`s!

This was thought to be a styling problem and should be fixed in CSS. There was no reason to add a grouping element to HTML, as the semantics are already unambiguous without an additional element.

In October 2016 it became clear that CSS would not fix this in the foreseeable future, HTML was changed to allow `<div>` as a grouping element in `<dl>`. See https://github.com/whatwg/html/issues/1937 and https://github.com/whatwg/html/pull/1945

### Why are some presentational elements like `<b>`, `<i>` and `<small>` still included?

The inclusion of these elements is a largely pragmatic decision based upon their widespread usage, and their usefulness for use cases which are not covered by more specific elements.

While there are a number of common use cases for italics which are covered by more specific elements, such as emphasis (em), citations (cite), definitions (dfn) and variables (var), there are many other use cases which are not covered well by these elements. For example, a taxonomic designation, a technical term, an idiomatic phrase from another language, a thought, or a ship name.

Similarly, although a number of common use cases for bold text are also covered by more specific elements such as strong emphasis (strong), headings (h1-h6) or table headers (th); there are others which are not, such as key words in a document abstract or product names in a review.

Some people argue that in such cases, the span element should be used with an appropriate class name and associated stylesheet. However, the b and i elements provide for a reasonable fallback styling in environments that don't support stylesheets or which do not render visually, such as screen readers, and they also provide some indication that the text is somehow distinct from its surrounding content.

In essence, they convey distinct, though non-specific, semantics, which are to be determined by the reader in the context of their use. In other words, although they don't convey specific semantics by themselves, they indicate that that the content is somehow distinct from its surroundings and leaves the interpretation of the semantics up to the reader.

This is further explained in the article [The `<b>` and `<i>` Elements](http://lachy.id.au/log/2007/05/b-and-i)

Similarly, the small element is defined for content that is commonly typographically rendered in small print, and which often referred to as fine print. This could include copyright statements, disclaimers and other legal text commonly found at the end of a document.

#### But they are PRESENTATIONAL!

The problem with elements like `<font>` isn't that they are _presentational_ per se, it's that they are media-dependent (they apply to visual browsers but not to speech browsers). While `<b>`, `<i>` and `<small>` historically have been presentational, they are defined in a media-independent manner in HTML5. For example, `<small>` corresponds to the really quickly spoken part at the end of radio advertisements.

### The `<cite>` element should allow names of people to be marked up

From what some have seen, `<cite>` is almost always used to mean "italics". More careful authors have used the element to mark up names and titles, and some people have gone out of their way to only mark up citations.

So, we can't really decide what the element should be based on past practice, like we usually do.

This leaves the question of what is the most useful use we can put the element to, if we keep it. The conclusion so far has been that the most useful use for `<cite>` is as an element to allow typographic control over titles, since those are often made italics, and that semantic is roughly close to what it meant in previous versions, and happens to match at least one of the common uses for the element. Generally, however, names and titles aren't typeset the same way, so making the element apply to both would lead to confusing typography.

There are already many ways of marking up names already (e.g. the [hCard microformat](http://microformats.org/wiki/hcard), the microdata vCard vocabulary, `<span>` and class names, etc), if you really need it.

### Where's the harm in adding...?

Every feature we add to the Web platform has a cost:

* Implementation: someone has to write code for it in each browser
* Testing: someone has to write the tests to check the features is working
* QA: someone has to regularly run the tests to make sure the feature doesn't regress
* Code maintenance: when browser vendors refactor code, they have to refactor more code if there's more features
* Tutorials: people who write tutorials have to include the feature, or handle feedback asking for them to do so
* Cognitive load: authors learning the platform have more documentation to wade through even if they don't care about the feature
* [Extra features discourage exploration](https://www.nngroup.com/articles/stagnating-expertise/): Having more features means less overall feature usage.
* Page maintenance: authors have to know how to maintain the feature if other people have used it in pages they now maintain
* Spec writing: someone has to write the spec for the feature and ensure it's maintained
* Bug fixing: when bugs are found in the spec or implementations, someone has to figure out a fix, implement it, test it, ship it, tests have to be fixed, documentation has to be updated, etc
* Code size: each feature increases the size of browsers (both on-disk binaries and in-memory resident size)

## WHATWG and the W3C HTML WG

### Are there plans to merge the groups?

No. The two groups have different goals. The WHATWG spec is intended to describe what browsers should aim for, introducing new features and describing reality in as much, and as accurate, detail as possible. The W3C spec is intended to follow the W3C process to REC.

On the WHATWG side, the editors read the feedback sent to both groups and take all input into account — and indeed there are far more places where input on HTML is sent than just these two mailing lists (e.g. blogs, www-html@w3.org, forums, direct mail, meetings, etc). (In particular, the editors do not look at the source of technical arguments when attempting to determine what path to take on an issue or other.)

### Which group has authority in the event of a dispute?

The two groups have different specs, so each has authority over its spec. The specs can and have diverged on some topics; unfortunately, these differences are not documented anywhere.

### Isn't it bad that the specs have forked?

Yes. The WHATWG originally committed to remaining consistent with the W3C spec unless the W3C working group showed a lapse in judgement. When that (in Hixie's opinion) occurred, there was little choice left but to let the specs diverge.

The plan to get the specs to converge again, such as it is, is to just do a better job with the WHATWG spec, such that it becomes the logical and obvious choice for anyone wanting to figure out which spec they should use.

### What is the history of HTML?

Here are some documents that detail the history of HTML:

* [A feature history of the modern Web Platform](https://platform.html5.org/history/) (2003 onward) ([on GitHub](https://github.com/whatwg/platform.html5.org/blob/master/history/index.html))
* [HTML's timeline on the ESW wiki](http://esw.w3.org/topic/HTML/history) (1997 to 2008)
* [The history section in the HTML standard itself](https://html.spec.whatwg.org/multipage/introduction.html#history-2)

## Using HTML

### Do you have any hints on how to use `<section>` and `<article>` and so on?

Some hopefully helpful hints:

* One way to look at it is how would you draw the page outline/table-of-contents? Each entry in the table of contents should be a `<section>`/`<article>`/`<aside>`/`<nav>`, and if it's not in the table of contents and doesn't have an `<h1>`, it should probably not be a `<section>`/`<article>`/`<aside>`/`<nav>`.
* You can still use `<div>`. It's the right element if you need a styling hook because CSS can't give you enough to do what you want.
* Generally, `<section>`s should start with an `<h1>` and the section title. It's not a hard-and-fast rule, but if you find yourself in a situation where an `<h1>` would be inappropriate, you probably want `<div>` rather than `<section>`.
* Sections can contain Articles, and vice versa. e.g. you can have a section that is news, a section that is editorials, a section that is sports, each with many articles, and each of those can have subsections, and each section can have comments, which are marked up using `<article>`, and each comment could be big enough that it has separate `<section>`s, and so on.

## Other specifications

### What ever happened to...?

The Web Forms 2.0 specification was folded into what is now the HTML specification.

The Web Controls 1.0 specification was overtaken by events and has been abandoned. Its problem space is mostly handled by ARIA and Web Components now.

The DOM Parsing specification was abandoned by the WHATWG because the W3C was doing a better job of maintaining that specification. We do not want to cause confusion in the market place, so when another organisation writes a specification that covers the same technology as one of ours, we only continue to publish it if our version is technically superior.