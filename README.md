Software Documentation Template
=================================
This is a template to generate software documentation from textual
files written in Markdown and/or RestructuredText.
The template is compliant with Sphinx and therefore the documentation can be
generated in different formats as convenient: HTML, PDF, ePub, Latex, etc.

It has been extended from the the ReadTheDocs template and therefore
your can be hosted out-of-the-box on the [ReadTheDocs](https://readthedocs.org/) website.

Diagrams written using PlantUML or Graphviz are rendered automatically
by [Sphinx](sphinx-doc.org) 


Installation
----------------


    # Create a python virtual environment
    virtualenv-3.5 venv-py35
        
    # Load environment
    source venv-py35/bin/activate
        
    # Install all dependencies
    pip install -r requirements.txt
        
    # To unload environment
    deactivate



Diagrams are generated by Sphinx automatically if they are coded in GraphViz 
or PlantUML. ReadTheDocs integrates support for both format in their docker 
images that will go live in production in 2017.
PlantUML is included for your convenience as [git-lfs](https://git-lfs.github.com/)
in ```utils/plantuml.jar```. 

Write you documentation
-----------------------
A base structure of a documentation is in the ```doc``` folder and is structured 
to document a software development project.
It is organised in sub folders and a hierarchy of RestructuredText files 
including or linking other ResT file or markdown.

The document files can be just in ResT format but we haven't found a reasonable support
 for editing them with a live preview as instead is for Markdown. On the other 
 hand Markdown doesn't support file inclusion that is a substantial limitation.
 
Therefore we use Markdown for all the documentation file except for the
files containing the table of contents or including other docs.

Editor
-----------
* PyCharm
* Eclipse


 Pycharm is a multi-platform and open source editor with two plugins helping our editing: Markdown split editor with one section for writing ode and one for live preview; the GfmBrowser supports page reloading upon change so any time you recompile the documentation you see the final ReadTheDocs pages.


 Eclipse has been identified as a multi-platform and open source editor with support for plantUML. Plugin supporting Markdown and ResT editing with live preview should be available but at the time of writing their installation was unsuccessful on Eclipse neon 2.0.


Generate your documentation in any of yor preferred formats (html, latex, pdf, epub)

    cd docs
    
    # Generate Html documentation
    make html
    
    # Open documentation with a Web browser
    firefox docs/_build/html/index.html
    



Deploy on ReadTheDocs
----------------------

ReadTheDocs hosts for you version of your documentation that is rebuild 
automatically everytime you commit a change.
Go to https://readthedocs.org/ and setup your account.
If your documentation is not a public git repository, use the 
[ReadTheDocs manual import](https://readthedocs.org/dashboard/import/manual/?)


Contribute
----------
Contributions are welcome. Open an Issue in the git repository and/or a
git pull request.

Support and bugs
----------------

If you are having issues, please let open an issue on this documentation
 git repository or email contributors.

License
-------

The project is licensed under the BSD license.
