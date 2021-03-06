# pyjst : Python Json simple Templating

Bake a template from corresponding JSON object

**Warning** : after some experience, JSON is _NOT_ Pythonic. Use YAML instead.

## How to use

Install (Python 3) : `pip install pyjst`

Create a project directory with given structure :
- project_name/
    - datas/
    - templates/

In **templates/** you can put templates with extension **.html**. In **datas/** you can put
corresponding data with extension **.json**. What this module does is simply render asked template
_name.tmpl_ with corresponding data _name.json_. The output is generated in folder **output/**.

For instance let this file tree :
- example/
    - datas/
        - example.json
        - another.json
    - templates/
        - example.tmpl
        - another.tmpl

So go into your project folder : `cd example`

Then generate your static page _example_ : `pyjst example`

Or generate static page _another_ : `pyjst another`

You can specify more to the command (templates folder, output file path, JSON data file path),
use `pyjst -h` to know how to use it.
