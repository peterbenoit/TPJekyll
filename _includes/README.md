# Server Side Includes ( SSIs )

This README is an attempt to document all of the Server Side Includes within the Template Package and WCMS. <br> 
Organized by placement in the index.html file.<br>

## Demo Index files
In the root of the repository you will find a **demo** folder full of index.html files. These provide examples of the markup that makes up the entire page for all the different templates the TP team provides.
```bash
├── cdciconfont.html - auto generated file from cdciconfont build
├── demo-atsdr.html - ATSDR index demo
├── demo-cards.html - cards demo, used with testing IE/chrome 
├── demo-footerslim.html - index demo with slim footer
├── demo-homepage.html - Homepage index demo
├── demo-index.html - Main index demo
├── demo-intranet.html - Intranet index demo
├── demo-ssi.html - SSI visual representation of default index demo
```

There are a couple of different index.html examples. 
1. Default index.html - Regular page template with left nav. 
2. Home page template - CDC Homepage example with top nav, fullwidth content area, and language assistance footer. No breadcrumbs or page share (hidden via Twitter Bootstrap class "d-none").
3. ATSDR template - Regular page template with modified Logo, search, and Footer.
4. Intranet template - Regular page template with static theme color, modified top navigation, and modified footer.

## SSI organization in the source

```bash
├── esp
│   ├── footer-agency.html
│   ├── footer-atsdr.html
│   ├── footer-cdc.html
│   ├── footer.html
│   ├── footer-language-assistance.html
│   ├── gov-delivery.html
│   ├── header-atsdr-logo.html
│   ├── header-home-logo.html
│   ├── header-local-search-example.html
│   ├── header-local-search-example-thirdlevelenav.html
│   ├── header-logo.html
│   ├── header-search-atsdr.html
│   ├── header-search.html
│   ├── header-search-v2.html
│   ├── last-reviewed.html
│   └── page-format.html
├── global
│   ├── body
│   │   ├── feature-area.html
│   │   ├── global-alert.html
│   │   ├── last-reviewed.html
│   │   ├── mobile-share-bar.html
│   │   ├── page-bottom-extras.html
│   │   ├── page-format.html
│   │   └── page-share.html
│   ├── footer
│   │   ├── footer-agency.html
│   │   ├── footer-atsdr.html
│   │   ├── footer-cdc.html
│   │   ├── footer.html
│   │   ├── footer-intranet-bottom.html
│   │   ├── footer-intranet-top.html
│   │   ├── footer-language-assistance-ATSDR.html
│   │   ├── footer-language-assistance.html
│   │   ├── footer-slim.html
│   │   ├── scripts.html
│   │   ├── scripts-syndication.html
│   │   └── social-media-footer.html
│   ├── header
│   │   ├── head-content.html
│   │   ├── head-content-meta-local.html
│   │   ├── head-content-syndication.html
│   │   ├── header-atsdr-logo.html
│   │   ├── header-home-logo.html
│   │   ├── header-intranet.html
│   │   ├── header-intranet-v2.html
│   │   ├── header-local-search-example.html
│   │   ├── header-logo.html
│   │   ├── header-search-atsdr.html
│   │   └── header-search.html
│   └── SVG
│       ├── svg-audio.html
│       ├── svg-esp-symbols.html
│       ├── svg-file-types.html
│       ├── svg-intranet-symbols.html
│       ├── svg-linear-gradients.html
│       ├── svg-multicolor.html
│       ├── svg-other.html
│       ├── svg-round-social.html
│       ├── svg-symbols.html
│       └── svg-white-social.html
├── local
│   ├── gov-delivery.html
│   ├── metrics.html
│   ├── metrics-intranet.html
│   ├── nav-breadcrumb.html
│   ├── nav-intranet.html
│   ├── nav-main.html
│   ├── nav-mobile.html
│   ├── nav-top.html
│   ├── nav-top-intranet.html
│   ├── persistent-content-area.html
│   ├── site-title.html
│   └── under-nav-left.html

```

## HTML Structure
Below are examples of how the HTML should be structured around each SSI.

### Head Content ( 1 )
Refer to demo-index.html file for example. This does not change between other templates. 

### Head Content Meta Local ( 2 )
Refer to demo-index.html file for example. This does not change between other templates. 

### Global Alert ( 3 )
Refer to demo-index.html file for example. This does not change between other templates.

### Header Bar ( 4, 5 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- (3) Header Bar -->
<div class="container-fluid header-wrapper">
    <div class="">
        <header role="banner" aria-label="Header" class="pt-2 pb-2">
            <div class="row">
                <div class="col cdc-logo">
                    <!-- Begin included content (from /TemplatePackage/4.0/includes/header-logo.html) -->
                    <!--#include virtual="../includes/header-logo.html" -->
                    <!-- End included content (from /TemplatePackage/4.0/includes/header-logo.html) -->
                </div>
                <div class="col-2 col-md-3 col-xl-4 col-xxl-3 tp-search">
                    <!-- Begin included content (from /TemplatePackage/4.0/includes/header-search.html) -->
                    <!--#include virtual="../includes/header-search.html" -->
                    <!-- End included content (from /TemplatePackage/4.0/includes/header-search.html) -->
                </div>
            </div>
        </header>
    </div>
</div>
```
</details>

### Site Title / Site Identity ( 6 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- (5 and 6) Site Title / Identity Area -->
<div class="container-fluid site-title">
    <a href="/TemplatePackage/4.0/gallery-internal/">
        <div class="">
            <div class="row">
                <div class="col">
                    <!-- (5) Site Title -->
                    <div class="display-6 text-white fw-500">Template Package 4: <i>Documentation</i></div>
                    <p class="tagline d-none d-md-inline-block">CDC Internal Use Only.</p>
                </div>
            </div>
        </div>
    </a>
</div>
```
</details>

### Mobile Nav ( 7 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- (7) Mobile Nav -->
<nav role="navigation" aria-label="Mobile Nav" id="mobilenav" class="sticky-top">
	<!-- Begin included content (from /TemplatePackage/4.0/includes/nav-mobile.html) -->
	<!--#include virtual="../includes/nav-mobile.html" -->
	<!-- End included content (from /TemplatePackage/4.0/includes/nav-mobile.html) -->
</nav>
```
</details>

### Breadcrumbs / Page Share ( 8, 9 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- (8 and 9) Breadcrumbs and Page Share Area  -->
<div class=" container-fluid breadcrumb-share">
	<div class="d-none d-lg-block">
		<div class="row">
			<!-- (8) Breadcrumbs Area -->
			<div class="col-sm-8 col-xl-9">
				<!-- Begin included content (from /TemplatePackage/4.0/includes/nav-breadcrumb.html) -->
				<!--#include virtual="../includes/nav-breadcrumb.html" -->
				<!-- End included content (from /TemplatePackage/4.0/includes/nav-breadcrumb.html) -->
			</div>
			<!-- (9) Page Share -->
			<div class="col-sm-4 col-xl-3 page-share">
				<!-- Page Share -->
				<!-- Begin included content (from /TemplatePackage/4.0/includes/page-share.html) -->
				<!--#include virtual="../includes/page-share.html" -->
				<!-- End included content (from /TemplatePackage/4.0/includes/page-share.html) -->
			</div>
		</div>
	</div>
</div>
```
</details>

### Feature Area ( 10 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- (10) Feature Area -->
<div class="container-fluid feature-area">
</div>
```
</details>


### Page Wrap ( 11, 12, 13, 14, 15, 16, 17, 18, 19 )
<details>
    <summary>HTML Structure</summary>
    
```bash
<!-- Page Content Wrap (11 through 19) -->
<div class=" d-flex flex-wrap body-wrapper">

	<!-- Content (11 through 19) -->
	<main class="col-lg-7 order-lg-2" role="main" aria-label="Main Content Area">
		<!-- (11) Visual Element -->
		<div class="row d-none d-md-block visual-element">
		</div>
		<!-- (12) Audience Identity -->
		<div class="row audience-identity">
			<!-- audience identity -->
		</div>

		<!-- (DEV ONLY) Section Nav Area -->
		<div class="docs-right-rail">
			<nav role="navigation" aria-label="Section Nav" class="w-100 d-md-none sticky-top">
				<!-- (13) Page Title/Section Nav (mobile) -->
			</nav>
		</div>

		<!-- (14) Content Area -->
		<div class="row">
			<div class="col content">
				<!-- Page Title -->
				<!-- Page Language
				(will bee included in content as needed)
				-->
				<!-- Content Area -->
				<h1 id="content">TP Docs Home</h1>
				<p class="lead"><span class="mark mark-yellow">This is TODO.</span></p>
			</div>
		</div>
		<!-- (15) Page Format -->
		<div class="row">
			<div class="col page-format">
				View Page In:
				<a href="#"><svg class="icon x16" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><use xlink:href="#pdf"></use></svg><span class="file-details">PDF [150k]</span></a>
				<a href="#"><svg class="icon x16" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><use xlink:href="#word"></use></svg><span class="file-details">DOC [150k]</span></a>
			</div>
		</div>

		<!-- (16) Persistent Content Area -->
		<div class="row">
			<!--#include virtual="../includes/persistent-content-area.html" -->
		</div>

		<!-- (17) Date Updated -->
		<div class="row">
			<div class="col last-reviewed">
				<!--#include virtual="../includes/last-reviewed.html" -->
			</div>
		</div>
	</main>

	<!-- (18, 19, 20) Left Nav / Bottom Nav and Under Left Nav -->
	<div class="leftnav-wrapper col-lg-3 order-lg-1">
		<!-- (18) Left Nav (Bottom Nave on smaller viewports) -->
		<!-- Begin included content (from /TemplatePackage/4.0/includes/nav-main.html) -->
		<!--#include virtual="../includes/nav-main.html" -->
		<!-- End included content (from /TemplatePackage/4.0/includes/nav-main.html) -->
        
        <!-- (19) Gov Delivery / Adobe Campaign -->
		<!-- Begin included content (from /TemplatePackage/4.0/includes/gov-delivery.html) -->
		<!--#include virtual="../includes/gov-delivery.html" -->
		<!-- End included content (from /TemplatePackage/4.0/includes/gov-delivery.html) -->


		<!-- (20) Under Left Nav (Hidden when left nav shifts to bottom nav ) -->
		<div class="row d-md-none">
			<div class="col under-left-nav">
				<!-- Begin included content (from /TemplatePackage/4.0/includes/under-nav-left.html) -->
				<!--#include virtual="../includes/under-nav-left.html" -->
				<!-- End included content (from /TemplatePackage/4.0/includes/under-nav-left.html) -->
			</div>
		</div>
	</div>


	<div class="d-none d-lg-block col-lg-2 bd-toc order-md-3" id="sectionnav">
		<ul class="docs-right-rail">
		</ul>
	</div>
</div>
```
</details>

### Footer Area ( 21, 22, 23, 24 )
<details>
    <summary>HTML Structure</summary>
    
```bash

<!-- (21, 22, 23, 24) Footer Area -->
<!-- (21) Footer -->
<footer role="contentinfo" aria-label="Footer">

	<!-- (22) Footer CDC -->
	<div class="container-fluid footer-wrapper">
		<div class="container">
			<!-- Begin included content (from /TemplatePackage/4.0/includes/footer-cdc.html) -->
			<!--#include virtual="../includes/footer-cdc.html" -->
			<!-- End included content (from /TemplatePackage/4.0/includes/footer-cdc.html) -->
		</div>
	</div>

	<!-- (23) Sub-Footer -->
	<div class="container-fluid agency-footer">
		<div class="container">
			<!-- Begin included content (from /TemplatePackage/4.0/includes/footer-agency.html) -->
			<!--#include virtual="../includes/footer-agency.html" -->
			<!-- End included content (from /TemplatePackage/4.0/includes/footer-agency.html) -->
		</div>
	</div>

</footer>
```
</details>

## SSI Naming Conventions
~ - indicates that the SSI does not exist in the WCMS, or it is modified in the WCMS to allow the users to manage it within the system instead of static SSIs from the TP.

1. **Head Content SSI** <br>
WCMS: globalHead_TP4<br>
TP: head-content.html

1. **Head Content Meta Local** <br>
WCMS: ~<br>
TP: head-content-meta-local.html

1. **Global Alert** <br>
WCMS: globalAlert_TP4<br>
TP: global-alert.html

1. **Header Logo** <br>
WCMS: globalHeaderLogo_TP4<br>
TP: header-logo.html <br>
globalHeaderHomeLogo_TP4 - header-home-logo.html<br>
globalIntranetHeader_TP4 - header-intranet-v2.html<br>
globalATSDRLogo_TP4 - header-atsdr-logo.html

1. **Header Search** <br>
WCMS: globalHeaderSearch_TP4<br>
TP: header-search.html <br>
globalATSDRSearch_TP4 - header-search-atsdr.html

1. **Site Title** <br>
WCMS: ~localSiteTitleBar_TP4<br>
TP: site-title.html

1. **Nav Mobile** <br>
WCMS: globalMobileNav_TP4<br>
TP: nav-mobile.html

1. **Nav Breadcrumbs** <br>
WCMS: ~localBreadcrumbs_TP4<br>
TP: nav-breadcrumb.html

1. **Page Share** <br>
WCMS: globalPageShare_TP4<br>
TP: page-share.html

1. **Feature Area** (home page only)<br>
WCMS: ~
TP: feature-area.html

1. **Visual Element** <br>
WCMS ~localVisualElement_TP4<br>
TP: ( visual element )

1. **Audience Identity** <br>
WCMS: ~<br>
TP: ( audience identity )

1. **Section Nav** <br>
WCMS: ~<br>
TP: ( section nav )

1. **Content Area** <br>
WCMS: ~<br>
TP: ( content area )<br>
(page title, page language, content area)

1. **Page Format** <br>
WCMS: ~<br>
TP: page-format.html

1. **Persistent Content Area** <br>
WCMS: ~localPersistentContentArea_TP4<br>
TP: persistent-content-area.html

1. **Last Reviewed** <br>
WCMS: ~<br>
TP: last-reviewed.html

1. **Nav Main** <br>
WCMS: ~localLeftNav_TP4<br>
TP:nav-main.html <br>
globalIntranetHeaderNav_TP4 - nav-intranet.html

1. **Gov Delivery/Adobe Campaign** <br>
WCMS: ~localGovDelivery_TP4<br>
TP: gov-delivery.html

1. **Under Left Nav** <br>
WCMS: ~localUnderNavDesktop_TP4, localUnderNav_TP4<br>
TP: under-left-nav.html

1. **Footer** <br>
WCMS: globalFooter_TP4<br>
TP: footer.html <br>
**Notes: This is not used.** <br>
globalATSDRFooter_TP4 - footer-atsdr.html
- footer-slim.html can be used instead of the follow three SSIs. Check above for HTML structure.

1. **Footer CDC** <br>
WCMS: globalFooterCDC_TP4<br>
TP: footer-cdc.html<br>
globalIntranetFooterTop_TP4 - footer-intranet-top.html

1. **Footer Agency** <br>
WCMS: globalFooterAgency_TP4<br>
TP: footer-agency.html <br>
globalIntranetFooterBottom_TP4 - footer-intranet-bottom.html

1. **Footer Language Assistance** <br>
WCMS: globalLanguageAssistance_TP4<br>
TP: footer-language-assistance.html <br>
globalLanguageAssistanceATSDAR_TP4 - footer-language-assistance-atsdr.html

1. **Social Media Footer** <br>
WCMS: globalFooterSocialMedia_TP4<br>
TP: social-media-footer.html

1. **PageBottom Extras** <br>
WCMS: globalPageBottomExtras_TP4<br>
TP: page-bottom-extras.html

1. **Scripts SSI** <br>
WCMS: globalScripts_TP4<br>
TP: scripts.html

1. **SVG SSIs** <br>
globalSVGSymbols_TP4 - svg-symbols.html <br>
globalSVGSymbolsAudio_TP4 - svg-audio.html <br>
globalSVGSymbolsIntranet_TP4 - svg-intranet-symbols <br>
globalSVGGradients_TP4 - svg-linear-gradients.html <br>
globalSVGSymbolsSMRound_TP4 - svg-round-social.html <br>
globalSVGSymbolsSMWhite_TP4 - svg-white-social.html <br>
globalSVGSymbolsOther_TP4 - svg-other.html <br>
svg-file-types.html

1. **Metrics** <br>
WCMS: globalMetrics_TP4<br>
TP: metrics.html <br>
globalMetricsIntranet_TP4 - metrics-intranet.html



## How to add CSS or JS to the Template Package
Every CSS link and JS script tag is either included in the head-content.html or scripts.html SSI for inclusion.


### How to conditionally include CSS in head-content.html
 
First you must open the head-content.html file in ./src/ssi/global/header/head-content.html,<br>
and place a new token in the file to be replaced when the build happens. Eg. 
```bash 
<!-- @newCSS@ --> 
```

Go to gulpfile.js<br>
Look for "replaceCSSlinks" function if applying CSS to "local", "intradev", or "intralink" targets<br>
Look for "replaceCSSlinksWWWDEV" function if applying to "wwwdev" target<br>
Look for "replaceCSSlinksProd" function if applying to "link"/prod target<br>

Then do a replace line with the new token and replace it with the script tag or filename if necessary.<br>
eg. 
```bash
.pipe( replace( '<!-- @newCSS@ -->', '<link rel="stylesheet" href="/TemplatePackage/contrib/libs/new/css/file.css" />' ) )
```

Then test by running "gulp" and see if the head-content.html SSI has been updated.


### How to conditionally include JS in scripts.html SSI

First you must open the scripts.html file in ./src/ssi/global/footer/scripts.html,<br>
and place a new token in the file to be replaced when the build happens. Eg. 
```bash 
<!-- @newJS@ --> 
```

Go to gulpfile.js<br>
Look for "replaceJSscripts" function if applying CSS to "local" target<br>
Look for "replaceJSscriptsWWWDEV" function if applying to "wwwdev" target<br>
Look for "replaceJSscriptsIntraDev" function if applying to "intradev" target<br>
Look for "replaceJSscriptsIntra" function if applying to "intralink" target<br>
Look for "replaceJSscriptsProd" function if applying to "link"/prod target<br>

Then do a replace line with the new token and replace it with the script tag or filename if necessary.<br>
eg. 
```bash
.pipe( replace( '<!-- @newJS@ -->', '<script src="/TemplatePackage/contrib/libs/new/js/file.js"></script>' ) )
```

Then test by running "gulp" and see if the scripts.html SSI has been updated.


## FAQs

#### What are Server Side Includes?
The original use for the SSIs was created because our WCMS product publishes content in a static process and we knew that certain things like the header and footer would almost never get updated and/or changed. <br>
Therefore for all the sections of the page that do not have frequent changes we turned into SSIs to avoid having to republish the entire page to produce content updates.  <br>
This also serves as another benefit to any app developers trying to use the Templates in their project. Centers at the CDC are strongly advised to use our TemplatePackage Templates in their apps, and we needed to provide a way for them to replace certain section of the page based on their app's needs.<br>

#### Why are Server Side includes important?
Server Side Includes provide editable sections of the HTML markup that make up the page of an app. 

#### How should I use Server Side Includes?
CDC app developers should rely heavily on the SSIs we have in place. <br>
**Only in very particular circumstances should you try to replace an SSI with one of your own.**<br>

#### How can I replace a SSI with one of my own?
 If an app developer needs to replace an SSI with one of their own, they should:
 1. create an SSI with the same name (or similar)
 1. Take the content of the original SSI and paste it into the new SSI (then make your changes)
 1. place it in the same folder or a new one and change the reference to the new location

#### How do I create a spanish version of a SSI?
Create a file or duplicate a SSI into the esp folder with the same name. <br>
Eg. globals/footer/footer-slim.html -> esp/footer-slim.html<br>
Then change the method "CDC_GLOBAL_INCLUDE_PATHS_ES" in the WCMS theme ( ../docroot/wp-content/themes/cdc-gov/constants.php ) to include the new Spanish SSI names. 
