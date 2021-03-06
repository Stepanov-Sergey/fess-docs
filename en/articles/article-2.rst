===========================================================
In |Fess| make Apache Solr based search Server-Mobile Edition
===========================================================

This page is generated by Machine Translation from Japanese.

Introduction
============

The last time\ `Introduction
chapter <http://codezine.jp/article/detail/4526>`__\ So, how to build
open-source full-text search server by |Fess| introduced. |Fess| on docomo,
au and Softbank Mobile search so that introduce how to use this time.

In this article, explains |Fess| 8.1.0. About how to build a
|Fess| \ `Introduction
chapter <http://codezine.jp/article/detail/4526>`__\ Please see the.

Intended audience
=================

-  Those who want to build mobile terminal search system

-  Observed to add search functionality on existing cell sites

Required environment
====================

Regarding the content of this article in the following environment and
behavior verification.

-  Windows 7 (Service Pack1)

-  JDK 1.7.0\_21

Mobile Terminal for |Fess| 
========================

Available for mobile terminals in the full-text search system for
systematically following such response will become necessary.

1. To get the mobile device information, suitable for Terminal

2. You can specify a crawl when you create for user agents

3. Can include career information index information

4. View converted into Web-site if the content search results

In the |Fess| corresponds to all of the above. For processing first,
retrieving the phone\ `mobylet <http://mobylet.seasar.org/>`__\ Is
adopted. mobylet is a Java open source framework for building mobile Web
applications. You can view the results mobylet in docomo, au and
Softbank handsets to identify the appropriate terminals each.

You can with Web crawl settings set the user agent when the next crawl
search in |Fess| . You can crawl the user agent for career, to get their
sites for mobile phones. However, you must allow |Fess| server IP you are
IP restrictions for mobile site, mobile phone sites displaying. Also,
viewable results carrier terminal only in select the carriers you want
to display all selected Web crawl settings in the default [browser], but
that becomes possible.

(If you use the PC site Viewer, such as can be viewed is) cannot
normally see on mobile devices even if the search result Web-site, PC
site link appears in the search results. It is possible to use the
Google Wireless Transcoder in |Fess| . Google Wireless Transcoder is a
service provided by Google, Inc., PC site will convert your various
mobile phone. It is possible for simple settings in |Fess| , links Google
Wireless Transcoder to convert search results the search results use
smooth PC site.

Instructions for use on a mobile device
=======================================

|Fess| 8.1.0 installed and is running.

registration for DoCoMo Web crawl settings
------------------------------------------

create a Web crawl settings to display the search results only if you
searched for DoCoMo handsets.

Access and http://localhost:8080/fess/admin in the management page,
please login. By default user name and password are both admin. Select
the [Web] from the left of the admin page. For anything not registered
in the initial state, select Create new.

Select the [new]
|image0|

This time the mobile phone site is not that will crawl all the pages of
http://fess.codelibs.org/ja/ following. any mobile sites that can be
displayed in DoCoMo handsets instead of http://fess.codelibs.org/ja/ the
site URL specifies.

[Browser] and select only the DoCoMo so that appears only in docomo
handsets. If you want to display in AU and Softbank handset select them
here.

After the user agent be user-agent for docomo handsets. This time we
enter DoCoMo/2.0 P903i.

for DoCoMo Web crawl settings
|image1|

Then, click the [create] on the confirmation screen that can crawl to
register. Registration is possible to change from the Edit.

Mobile conversion configuration
-------------------------------

Sets the search results PC if there is Google Wireless Transcoder
available sites you like. Excluding the PC site to search for the mobile
site is just there if you don't need this setting.

Select the crawl General from the left of the admin page. In the mobile
conversion, select the Google Wireless Transcoder.

Mobile conversion configuration
|image2|

Saves the settings and click [update].

The index of
------------

Mobile handset settings after the start to crawl, create a searchable
index. Select the system settings from the left of the admin page.

System settings
|image3|

Click the start crawling, initiates a search for crawling and indexing.
While complete crawl.

Search
------

First, try searching in the PC browser, such as Internet Explorer. visit
http://localhost:8080/ |Fess| , locate the |Fess| .

Search in PC browser
|image4|

You can: set Web crawl settings in the PC browser in search results is
displayed.

The following access in docomo handsets. This time real terminal, not in
Firefox\ `FireMobileSimulator <http://firemobilesimulator.org/>`__\ Use
Add-ons, to see the results. FireMobileSimulator is a Firefox Add-on
that simulates the major three carriers mobile phone browser.
FireMobileSimulator installed in Firefox, from the Firefox menu select,
DC Terminal docomo P903i from [tool] [FireMobileSimulator]. When you
access this setting allows Firefox to simulate the P903i handset
environment. Similarly if the PC browser and visit
http://localhost:8080/fess, locate the |Fess| .

Search in DoCoMo handsets
|image5|

Search for this time is specified in the Web crawl settings is
displayed.

Summary
=======

How to respond to the |Fess| in the full-text search system handsets
introduced. I could introduce you can provide search functionality to
the handsets of three major carriers in simple settings. Also, it is
possible to respond by phone will be released new models on a regular
basis, but the latest terminal information file in |Fess| 
'webapps/fess/WEB-INF/classes/device'. About how to update the device
information file see the README in the directory.

Next switch to display results search results depending on
authentication of users, roles functions are introduced here.

Reference material
==================

-  `Fess <http://fess.codelibs.org/ja/>`__

-  `mobylet <http://mobylet.seasar.org/>`__

-  `FireMobileSimulator <http://firemobilesimulator.org/>`__

.. |image0| image:: ../../resources/images/en/article/2/web-crawl-conf-1.png
.. |image1| image:: ../../resources/images/en/article/2/web-crawl-conf-2.png
.. |image2| image:: ../../resources/images/en/article/2/crawl-conf-1.png
.. |image3| image:: ../../resources/images/en/article/2/system-1.png
.. |image4| image:: ../../resources/images/en/article/2/search-1.png
.. |image5| image:: ../../resources/images/en/article/2/search-2.png
