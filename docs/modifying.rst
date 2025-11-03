Modifying the Documentation
===========================

Setup
-----
1. Email your GitHub email to jreback@colostate.edu to receive edit permissions.
2. Install Visual Studio Code (VS Code): `Visual Studio Code <https://code.visualstudio.com/>`_
3. (Optional) Install GitHub Copilot in VS Code to get suggestions for .rst syntax.

Tip
~~~~
To make it easier to write these files, start your document in Word/Google Docs and export it as Markdown (.md).

Converting a Markdown (.md) file to reStructuredText (.rst)
-----------------------------------------------------------
1. Use the CloudConvert MD→RST converter: `CloudConvert MD→RST <https://cloudconvert.com/md-to-rst>`_
2. Upload your .md file and download the converted .rst output.
3. Copy the converted content into the ``docs/`` directory of this repository.
4. Manually add any images (see below).

Adding Images
-------------
1. Create an ``images`` folder inside the ``docs`` directory (if it doesn't exist).
2. Add your image files to that folder.
3. Reference images in your .rst files using the image directive:

.. code-block:: rst
    
   .. image:: images/your_image_file.png
      :alt: Alternate text for the image
      :align: center
      :width: 400px


Notes on editing
----------------
- Keep files inside the ``docs/`` folder so Sphinx/ReadTheDocs can find them.
- If this page is not referenced by your project's ``index.rst`` (or a toctree), add it there to include it in the built docs.
- Use RST hyperlink syntax ``( `text <url>`_ )`` instead of raw URLs for better rendering.



Once your .rst file is created or updated, commit and push it to the repository. 
You may need to get GitHub set up on your local machine if you haven't already. 
Here's a guide on doing that: `GitHub in VS Code <https://code.visualstudio.com/docs/sourcecontrol/github>`_


If you've done everything correctly, you can refresh the documentation webpage to see your changes. If you need more help, reach out to Joey Reback.