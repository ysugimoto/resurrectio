Resurrectio
===========

**Any phantom deserves a resurrection.**

Resurrectio is a Chrome extension allowing to record a sequence of browser
actions and to produce the corresponding `CasperJS  <http://casperjs.org/>`_
script.

Resurrectio uses minimalist and functional-oriented selectors, so recorded
sequences stay valid across layout and design changes.

As **CasperJS evaluates JavaScript**, recorded sequences are not limited
to pure HTML interactions, targeted pages JavaScript-supported behaviors will
be accurately reproduced.

Resurrectio also provides a way to produce **screenshots** alongside your test
scenario, and can export comments + screenshots in ReStructuredText format in
order to generate documentation automatically from the test sequences.

Installation
============

CasperJS / PhantomJS
--------------------

Install `PhantomJS <http://code.google.com/p/phantomjs/wiki/Installation>`_,
be careful CasperJS requires PhantomJS >= 1.8.2.

Install `CasperJS <http://casperjs.org/installation.html>`_ version 1.1.

Resurrectio installation
-------------------------

From Chrome store:

Go to `Chrome store Resurrectio page <https://chrome.google.com/webstore/detail/resurrectio/kicncbplfjgjlliddogifpohdhkbjogm>`_ and click on the Add button.

OR

From Github sources::

    git clone git://github.com/ebrehault/resurrectio.git

It will produce a ./resurrectio folder.

Then, in Chrome:

    - go to **Tools / Extensions**,
    - expand **Developer mode**,
    - click **Load unpacked extension**,
    - select the ./resurrectio folder.

Usage
=====

Click on the Resurrectio extension icon.

Enter the start URL, and click Go.

Then execute your usage scenario, all the events will be recorded.

By right-clicking on the page, you might also record some assertion (about the
current url, about existing text, etc.).

You can request a **screenshot** at any moment (they will be produced everytime
you run the resulting test).

You might also record some comments (click again on the extension icon, and
click **Add comment**).

When you are done, click again on the extension icon, and
click **Stop recording**.

Now, generate the CasperJS test script by clicking **Export Casper test**.

Copy/paste the resulting code into a local file, and run the test::

    casperjs test my_scenario.js

It will play your entire scenario and generate the screenshots.

Future features
===============

Implement more mouse events, like drag & drop and mousewheel.

Credits
=======

Author
------

* Eric BREHAULT <eric.brehault@makina-corpus.org>

* Resurrectio event recorder is based on the zope.recorder tool, created by Brian Lloyd <brian@zope.com>

Companies
---------
|makinacom|_

* `Makina Corpus blog <http://makina-corpus.com/blog/metier/>`_
* `Contact us <mailto:python@makina-corpus.org>`_


.. |makinacom| image:: http://depot.makina-corpus.org/public/logo.gif
.. _makinacom:  http://www.makina-corpus.com


.. image:: https://d2weczhvl823v0.cloudfront.net/ebrehault/resurrectio/trend.png
   :alt: Bitdeli badge
   :target: https://bitdeli.com/free

