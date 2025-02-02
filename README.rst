=============
google-search
=============

Library for scraping google search results.

* Usage::

    from googlesearch.googlesearch import GoogleSearch
    response = GoogleSearch().search("something")
    for result in response.results:
        print("Title: " + result.title)
        print("Content: " + result.getText())



* Free software: MIT license

Features
--------

Run a Google search and fetch the individual results (full HTML and text contents). By default the result URLs are fetched eagerly when the search request is made with 10 parallel requests. Fetching can be deferred until ``searchResult.getText()`` or ``getMarkup()`` are called by passing ``prefetch_results = False`` to the search method.

Pass ``num_results`` to the search method to set the maximum number of results. 

``SearchReponse.total`` gives the total number of results on Google.

Credits
---------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage