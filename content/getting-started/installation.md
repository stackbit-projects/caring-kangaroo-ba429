---
title: Installation
description: QB Pro Install
weight: 1
---
<h1 class="page-title">How to install QuickBox Pro &#8211; Standard Install</h1> </header>
<figure class="post-thumbnail"><a class="post-thumbnail__link" href="https://quickbox.io/knowledge-base/standard-install/" aria-hidden="true"><img width="370" height="265" src="https://quickbox.io/wp-content/uploads/2019/02/standard-install-370x265.png" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" alt="" /></a></figure>
<div class="page-content">

<div id="hkb" class="hkb-template-single">
<form class="hkb-site-search" method="get" action="https://quickbox.io/">
<label class="hkb-screen-reader-text" for="s">Search For</label>
<input class="hkb-site-search__field" type="text" value="" placeholder="Search the Knowledge Base" name="s" autocomplete="off">
<input type="hidden" name="ht-kb-search" value="1" />
<input type="hidden" name="lang" value="" />
<button class="hkb-site-search__button" type="submit"><span>Search</span></button>
</form>

<ol class="hkb-breadcrumbs" itemscope itemtype="https://schema.org/BreadcrumbList">
<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
<a itemprop="item" href="https://quickbox.io">
<span itemprop="name">Home</span>
</a>
<meta itemprop="position" content="1" />
</li>
<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
<a itemprop="item" href="https://quickbox.io/knowledge-base/">
<span itemprop="name">Knowledge Base</span>
</a>
<meta itemprop="position" content="2" />
</li>
<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
<a itemprop="item" href="https://quickbox.io/kb-categories/installation/">
<span itemprop="name">Installation</span>
</a>
<meta itemprop="position" content="3" />
</li>
<li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
<span>
<span itemprop="name">How to install QuickBox Pro &#8211; Standard Install</span>
<link itemprop="item" href="https://quickbox.io/knowledge-base/standard-install/" />
</span>
<meta itemprop="position" content="4" />
</li>
</ol>

<div class="hkb-entry-content">

<div class="hkb-article__content entry-content" itemprop="articleBody">
<div data-elementor-type="wp-post" data-elementor-id="17191" class="elementor elementor-17191" data-elementor-settings="[]">
<div class="elementor-inner">
<div class="elementor-section-wrap">
<section class="elementor-section elementor-top-section elementor-element elementor-element-4ab0bd2a elementor-section-boxed elementor-section-height-default elementor-section-height-default" data-id="4ab0bd2a" data-element_type="section">
<div class="elementor-container elementor-column-gap-default">
<div class="elementor-row">
<div class="elementor-column elementor-col-100 elementor-top-column elementor-element elementor-element-4b2395f1" data-id="4b2395f1" data-element_type="column">
<div class="elementor-column-wrap elementor-element-populated">
<div class="elementor-widget-wrap">
<div class="elementor-element elementor-element-44566c09 elementor-widget elementor-widget-text-editor" data-id="44566c09" data-element_type="widget" data-widget_type="text-editor.default">
<div class="elementor-widget-container">
<div class="elementor-text-editor elementor-clearfix"><p></p>
<p>This is for the installation of QuickBox Pro, for information on QuickBox Community see our Github <a href="https://github.com/QuickBox/QB" target="_blank" rel="noopener"><strong>HERE</strong></a>. Additional comparisons between CE (Community Edition) and Pro can be found <a href="https://quickbox.io/quickbox-edition-comparison/"><strong>HERE</strong></a>.</p>
<p>
</p>
<h3 id="supported-os-distro">Supported OS/Distro</h3>
<p>
</p>
<p><img class="alignnone" src="https://img.shields.io/badge/Ubuntu%2016.04-retired-black.svg?style=flat-square" alt="Ubuntu 16.04 retired" width="136" height="20" /> <img src="https://img.shields.io/badge/Ubuntu%2018.04-passing-brightgreen.svg?style=flat-square" alt="Ubuntu 18.04 Passing" /> <img src="https://img.shields.io/badge/Ubuntu%2020.04-passing-brightgreen.svg?style=flat-square" alt="Ubuntu 20.04 Passing" /> <img src="https://img.shields.io/badge/Debian%209-passing-brightgreen.svg?style=flat-square" alt="Debian 9 Passing" /> <img src="https://img.shields.io/badge/Debian%2010-passing-brightgreen.svg?style=flat-square" alt="Debian 10 Passing" /></p>
<p>
</p>
<hr class="wp-block-separator is-style-default" />
<p>
</p>
<h3 id="before-installation">Before installation</h3>
<p>
</p>
<p>You need to have a Fresh &#8220;blank&#8221; server installation. After that access your box using a SSH client, like PuTTY. Please run in root to avoid conflicts. Additionally, ensure that you have your QuickBox Pro API Key available, you can learn more about how to attain that <strong><a href="https://quickbox.io/knowledge-base/activating-your-quickbox-pro-api-key/">in this article</a></strong>.</p>
<p>
</p>
<p><strong>If you login to your server as sudo user, please run <code>sudo su -</code> to properly elevate your permissions to root. This is necessary to avoid potential permissions issues when building the database for QuickBox Pro.</strong></p>
<p>Also advisable to run below code to make certain your server has gotten a full update before stating the installation!</p>
<p>
</p>
<pre class="EnlighterJSRAW" data-enlighter-language="generic" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">apt-get -y update &amp;&amp; apt-get -y upgrade
apt-get -y install sudo dirmngr curl wget git net-tools iproute2</pre>
<p>
</p>
<hr class="wp-block-separator is-style-default" />
<p>
</p>
<h3 id="how-to-install">How to install</h3>
<p>
</p>
<div class="elementor-alert elementor-alert-info"><span class="elementor-alert-title">IMPORTANT NOTICE ABOUT INSTALLING</span> <br /><span class="elementor-alert-description">* DO NOT use a username that begins or ends with a numeric character or contains uppercase letters. This can cause issues with permissions as well as odd quirks within Linux that are undesirable. This is not a QuickBox limitation, rather this is a limitation with Linux and/or various applications. We have to make them happy in various ways, so best practice is to keep things simple.<br />
* DO NOT use usernames such as <strong>none</strong>, <strong>admin</strong>, <strong>root</strong> as these are system reserved and could cause breakage on certain functionality in QuickBox Pro. <strong>none</strong> in particular will fail with applications such as rtorrent that utilize screen as <strong>none</strong> is a pre-set variable.<br /> * Additionally, try to avoid using characters such as <code>!</code>, <code>\</code>, <code>/</code>, <code>+</code>, <code>@</code>, and <code>%</code> in usernames &amp; passwords on setup as this can cause an identifying issue within Linux. Please note however, that after installation is finished, you can edit your password to be much stronger as the dashboard password edit allows these additional characters.</span></div>
<p>
</p>
<h4 id="run-the-following-command-to-grab-our-latest-release">Run the following command to grab our latest release &#8230;</h4>
<p>
</p>
<p>Simply fill in the <code>USERNAME=</code>, <code>PASSWORD=</code>, and <code>API_KEY=</code> variables below, then copy and paste to get started on your install. DO NOT use any special characters in your username or password, as this will break the script from running. </p>
<p>
</p>
<pre class="EnlighterJSRAW" data-enlighter-language="generic" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">USERNAME=
PASSWORD=
API_KEY=
(apt-get -y update &amp;&amp; apt-get -y upgrade &amp;&amp; apt-get -y autoclean; \
apt-get -y install sudo dirmngr curl wget git net-tools iproute2; \
cd /root &amp;&amp; wget -q https://lab.quickbox.io/QuickBox/Pro/raw/master/qbpro &amp;&amp; chmod +x qbpro; \
./qbpro -u="${USERNAME}" -p="${PASSWORD}" -k="${API_KEY}";)</pre>
<p>
</p>
<hr class="wp-block-separator is-style-default" />
<p>
</p>
<h4 id="what-do-these-values-mean">What do these values mean?</h4>
<p>
</p>
<pre class="EnlighterJSRAW" data-enlighter-language="Markdown" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-title="" data-enlighter-group="">Options:
-u,    --username    The QuickBox primary user
-p,    --password    The QuickBox primary user password
-k,    --api_key     The API Key associated with your install
-ssh,  --ssh_port    The optional ssh port you would like to assign to your server
-ftp,  --ftp_port    The optional ftp port you would like to assign to your server
-m,    --mount       Custom mount point for HDD status on dashboard
       --reboot      Automatically reboot at end of setup
-h,    --help        Display this help and exit
-v,    --version     Output version information and exit</pre>
<p>
</p>
<hr class="wp-block-separator is-style-default" />
<p>
</p>
<h3 id="examples">Examples</h3>
<p>
</p>
<p><strong>Note that these fields are unique to your wants.</strong><br /><code>-u=YOURUSERNAME</code>, <br /><code>-p=YOURPASSWORD</code>, and <br /><code>-k=YOURAPIKEY</code> fields are required.</p>
<p>
</p>
<p><code>./qbpro -u="username" -p="password" -k="apikey"</code></p>
<p>
</p>