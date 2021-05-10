# plantuml-diagrams


[PlantUML](github.com/plantuml/plantuml) diagrams.

#### How to use

Use the PlantUML proxy service as described in this [stackoverflow discussion](https://stackoverflow.com/questions/32203610/how-to-integrate-uml-diagrams-into-gitlab-or-github) to display PlantUML diagrams in github markdown. Instead of passing diagram content within the URL,define a remote URL where the content can be fetched from, as e.g. [in a repo](http://www.plantuml.com/plantuml/proxy?src=https://raw.github.com/plantuml/plantuml-server/master/src/main/webapp/resource/test2diagrams.txt).
  
This URL can be embedded in an HTML `<img>` tag or a Markdown image syntax `![]()`. To leverage this feature when using GitHub, simply point the remote URL to a raw link of the PlantUML diagram in your repository.

* Adding a `?cache=no` might be a good idea because GitHubs caching will prevent your images from updating, if you change the sourcecode.
* The `&fmt=svg` can be used to change the format

The following diagram shows what will happen when you open a Markdown page hosted on GitHub that contains such a link:

```markdown
![uncached example1](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.githubusercontent.com/marcelofpfelix/plantuml-diagrams/master/example/example1.puml)

![uncached example2](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.githubusercontent.com/marcelofpfelix/plantuml-diagrams/master/example/example2.puml)
```

#### skin

You can use a link to choose a skin:

```plantuml
@startuml
!includeurl https://raw.githubusercontent.com/marcelofpfelix/plantuml-diagrams/master/skins/skin_clear.puml

(...)
@enduml
```

!includeurl https://raw.githubusercontent.com/bandonga/plantuml-diagrams/master/skin_clear.puml!0

##### Demo

![example1](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.githubusercontent.com/marcelofpfelix/plantuml-diagrams/master/example/example1.puml)

![example2](http://www.plantuml.com/plantuml/proxy?cache=no&fmt=svg&src=https://raw.githubusercontent.com/marcelofpfelix/plantuml-diagrams/master/example/example2.puml)


##### Alternatives
* [mermaid.js](https://github.com/knsv/mermaid), not avalailable on github markdown
* [draw.io](https://github.com/jgraph/drawio-github)

##### Resources
* [anoff.io](https://anoff.io/blog/2018-07-31-diagrams-with-plantuml/)
* https://www.planttext.com/
* https://plantuml-documentation.readthedocs.io/

