Templates documentation
=======================

.. _Templates.documentation::

Template dictionary
###################

To replace all templates, just change your templates folder with the same filenames. If you wish to replace only one template, you need to use those keys :

.. code-block:: python

    TEMPLATES = {
        "container": "container.html",
        "menu": "menu.html",
        "text": "text.html",
        "textgroups": "textgroups.html",
        "index": "index.html",
        "texts": "texts.html",
        "version": "version.html",
        "passage_footer": "passage_footer.html"
    }

Variables shared across templates
#################################

+-----------------+----------------------------------------------------------+
| Variable Name   | Details                                                  |
+=================+==========================================================+
| `assets['css']` | List of css files to link to.                            |
+-----------------+----------------------------------------------------------+
| `assets['js']`  | List of js files to link to.                             |
+-----------------+----------------------------------------------------------+
| `url[*]`        | Dictionary where keys and values are derived from routes |
+-----------------+----------------------------------------------------------+
| `templates[*]`  | Dictionary of templates with at least menu and container |
+-----------------+----------------------------------------------------------+
| `collections`   | Collections list                                         |
+-----------------+----------------------------------------------------------+
| `lang`          | Lang to display                                          |
+-----------------+----------------------------------------------------------+

index.html
##########

Only `Variables shared across templates`_

menu.html
#########

Only `Variables shared across templates`_

textgroups.html
###############

See `r_collection` in :ref:`Nemo.api.r_collection`

+-----------------+----------------------------------------------------------+
| Variable Name   | Details                                                  |
+=================+==========================================================+
| `textgroups`    | List of textgroups according to a collection             |
+-----------------+----------------------------------------------------------+

texts.html
##########

See `r_texts` in :ref:`Nemo.api.r_texts`

+-----------------+----------------------------------------------------------+
| Variable Name   | Details                                                  |
+=================+==========================================================+
| `texts`         | List of texts according to a textgroup                   |
+-----------------+----------------------------------------------------------+

version.html
############

See `r_version` in :ref:`Nemo.api.r_version`

+-----------------+-----------------------------------------------------------------------------------------+
| Variable Name   | Details                                                                                 |
+=================+=========================================================================================+
| `version`       | Version object with metadata about current text                                         |
+-----------------+-----------------------------------------------------------------------------------------+
| `reffs`         | List of tuples where first element is a reference, second a human readable translation  |
+-----------------+-----------------------------------------------------------------------------------------+

text.html
#########


See `r_passage` in :ref:`Nemo.api.r_passage`

+-----------------+----------------------------------------------------------------------------------------+
| Variable Name   | Details                                                                                |
+=================+========================================================================================+
| `version`       | Version object with metadata about current text                                        |
+-----------------+----------------------------------------------------------------------------------------+
| `text_passage`  | Markup object representing the text                                                    |
+-----------------+----------------------------------------------------------------------------------------+
| `urn`  | Markup object containing the URN of the passage for display
+-----------------+----------------------------------------------------------------------------------------+
| `prev`          | Previous Passage Reference                                                             |
+-----------------+----------------------------------------------------------------------------------------+
| `next`          | Following Passage Reference                                                            |
+-----------------+----------------------------------------------------------------------------------------+

passage_footer.html
#########


See `r_passage` in :ref:`Nemo.api.r_passage`

+-----------------+----------------------------------------------------------------------------------------+
| Variable Name   | Details                                                                                |
+=================+========================================================================================+
| `version`       | Version object with metadata about current text                                        |
+-----------------+----------------------------------------------------------------------------------------+
| `text_passage`  | Markup object representing the text                                                    |
+-----------------+----------------------------------------------------------------------------------------+
| `urn`  | Markup object containing the URN of the passage for display
+-----------------+----------------------------------------------------------------------------------------+
| `prev`          | Previous Passage Reference                                                             |
+-----------------+----------------------------------------------------------------------------------------+
